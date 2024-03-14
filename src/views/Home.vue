<template>
  <h1>Home</h1>
  <p class="text-3xl text-amber-200">Welcome to the home page2!</p>
</template>


<script>

import {onMounted, ref} from "vue";
import axios from "axios";

export default {
  name: 'Home',
  setup() {
    const message = ref('Hello, Vue 3!')
    onMounted(async  () => {
     const {data} = await axios.get('users', {
       headers: {
         'Content-Type': 'application/json',
       },
       withCredentials: true,
    })
    console.log(data);
        return {
      isLogin: false
    }
  })
}}

</script>