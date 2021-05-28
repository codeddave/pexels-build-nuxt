<template>
  <div class="c overflo-hidden flex flex-col">
    <Hero/>
    <Menu/>
    <div class="px-6 md:pl-10">
      <p class="pt-4 font-bold text-gray-600 text-xl">Free Stock Photos</p>

    <div class="grid grid-cols-2 md:grid-cols-4 grid-rows-1 pt-4 gap-x-4 gap-y-4 ">
        <Picture v-for="picture in pictures" v-bind:key="picture.id" :picture="picture.src.original"/>
    </div>
    </div>
  </div>
</template>

<script>
import Hero from '../components/Hero.vue'
import Menu from '../components/Menu.vue'
import Picture from '../components/Picture.vue'

import axios from 'axios'
export default {
  components: {
    Hero, 
    Menu,
    Picture
  }, 
  data() {
    return {
      pictures: []
    }
  },

  async created(){
    const config = {
      headers: {
        "Authorization": process.env.NUXT_ENV_API_KEY
      }
    }
    try{
      const res = await axios.get("https://api.pexels.com/v1/curated", config)
      this.pictures = res.data.photos
      console.log(res.data)
         console.log(res.data.photos[0].url)
    }catch(error) {
      console.log(error)
    }
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/


</style>
