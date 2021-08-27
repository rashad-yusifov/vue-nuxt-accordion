<template>
  <div id="app">
    <V-accordion>
          <template v-slot:title>
            <span
             style="color: white"
              >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Turpis
              feugiat velit feugiat quis. In.</span
            >
          </template>
          <template v-slot:content>
            <span style="color: white">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Suscipit
              consequuntur quasi sapiente vero? Possimus similique nesciunt nostrum
              temporibus quia vitae corrupti recusandae magni corporis hic modi rem
              doloribus ea id, ad distinctio qui quis accusamus accusantium animi
              veniam.
            </span>
          </template>
    </V-accordion>
  </div>
</template>

<script>
import Vaccordion from '@/components/Accordion.vue';
export default {
  name: 'App',
  components: {
    'V-accordion': Vaccordion
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
