<template>
  <div class="c">
    <Hero/>
    <div class="pictures-container"> 
        <Picture v-for="picture in pictures" v-bind:key="picture.id" :picture="picture.url"/>
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
        "Authorization": "563492ad6f9170000100000197e2f629736443e4863dc69bffc419d5"
      }
    }
    try{
      const res = await axios.get("https://api.pexels.com/v1/curated", config)
      this.pictures = res.data.photos
      console.log(res.data)
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
