<template>
  <div class="accordion-box v-accordion-box" :class="{active: isOpen}">
    <div class="accordion-head" @click="isOpen = !isOpen">
      <div class="title-accordion">
        <slot name="title" />
      </div>
      <div class="right-icon">
        <slot name="icon" v-if="$slots['icon']" />
        <svg
          v-else
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
        >
          <path
            d="M6 9L12 15L18 9"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </div>
    </div>
    <div class="accordion-content" v-if="isOpen">
        <div class="v-content">
            <slot name="content"/>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return {
            isOpen: false
        }
    },
    watch: {
        isOpen(value){
            this.$emit('isActive', value)
        }
    },
    mounted(){
        let _this = this;
        this.$root.$emit('close', function(){
            _this.isOpen = false;
        });
        window.addEventListener('click', (e) => {
            if (!this.$el.contains(e.target)){
                _this.isOpen = false;
            }
        })
    }
};
</script>
<style scoped>
.accordion-box {
  width: 100%;
  position: relative;
}
.accordion-box.active .accordion-head{
    padding-bottom: 24px;
}
.accordion-box.active .right-icon svg{
    transition: 0.3s;
    transform: rotateX(-180deg);
}
.right-icon svg{
    transition: 0.3s;
}
.accordion-content{
    background: #1a1a1a;
    width: 100%;
    position: relative;
    max-height: 370px;
    overflow: auto;
    padding-bottom: 30px;
}
.accordion-box .v-content{
    text-align: start;
    padding-right: 30px;
    padding-left: 30px;
}
.accordion-head {
  position: relative;
  text-align: start;
  padding: 30px;
  cursor: pointer;
  padding-right: 80px;
  background: #1a1a1a;
  display: flex;
  align-items: center;
}
/* .title-accordion {
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
} */
.title-accordion * {
  margin: 0;
}
.accordion-head .right-icon {
  display: flex;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  right: 30px;
}
@media screen and (max-width: 500px){
    .accordion-head{
        padding-top: 24px;
        padding-left: 16px;
        padding-right: 54px;
    }
    .accordion-box{
        width: 100%;
    }
    .right-icon{
        top: 24px !important;
        right: 16px !important;
        transform: inherit !important;
    }
    .v-content{
        padding-right: 16px !important;
        padding-left: 16px !important;
    }
}
</style>
