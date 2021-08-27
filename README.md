# v-accordion

## If you want install only package
```
npm i vue-nuxt-accordion --save
```

## You will make the add-ons yourself, you can download the repository.

```
https://github.com/Rashad-Yusifov/v-accordion.git
```


## How to use component ? (example)

```
<template>
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
</template>

<script>
import Vaccordion from 'v-accordion';
export default {
  components: {
    'V-accordion': Vaccordion
  }
}
</script>

```


## Accepted slots property (TITLE) | required

```
<template v-slot:title>
        <span
          >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Turpis
          feugiat velit feugiat quis. In.</span>
 </template>
```



## Accepted slots property (accordion content) | required

```
<template v-slot:content>
    <span >
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Suscipit
        illo repellat quod recusandae expedita? Porro exercitationem
        aspernatur repellat earum voluptates aliquam blanditiis ut, inventore.
    </span>
</template>
```



## Accepted slots property (Custom arrow icon)

```
<template v-slot:icon>
        <svg
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M6 9L12 15L18 9"
            stroke="white"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
 </template>
```



## Thanks for downloading.
