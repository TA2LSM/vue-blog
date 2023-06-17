<template>
  <div class="home">
    <p ref="refP">Name: {{ name }}, Age: {{ age }}</p>

    <button @click="handleClick">
      Click me!
    </button>
  </div>
</template>

<script>
import { ref } from 'vue'

// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  
  // 1st order
  setup() {
    // values in setup are not reactive values
       
    // let name_in_setup = 'ta2lsm'
    // let age_in_setup = 39
    // return { name: name_in_setup, age: age_in_setup}
    
    // variables
    let name = 'ta2lsm'
    let age = 39

    // functions
    const handleClick = () => {
      // console.log('Button clicked')
      console.log("refP: ", refP)
      console.log("refP Value: ", refP.value)
    }

    // refs
    const refP = ref(null)    // 15. dk devam

    return { name, age, handleClick, refP }
  },
  // // 2nd order
  // data() {
  //   // values in data are reactive values. Changes of them will be reflected in template
  //   // ...
  // },
  // // 3rd order
  // created() {

  // },
  // // 4th order
  // mounted() {

  // }
}
</script>
