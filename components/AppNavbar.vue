<template lang="">
    <div class=" sticky top-0 -mt-20  z-50 py-3 flex justify-between items-center text-white font-bold w-full text-lg navvv">
        <div> 
            <p class="pl-4">Pexels</p>
        </div>
        <div class="flex "> 
            <ul class=" hidden md:flex justify-center w-full items-center"> 
                <li class="pr-6"> Explore </li>
                  <li class="pr-6"> License</li>
                    <li class="pr-6"> <span class="icon is-left "><font-awesome-icon class="" :icon="['fa', 'bell']"> </font-awesome-icon></span></li>
                      <li class="pr-6"><span class="icon is-left "><font-awesome-icon class="" :icon="['fa', 'user-circle']"> </font-awesome-icon></span></li>
                      <li><button class="bg-green-600 px-4 h-10  mr-6 rounded font-bold"> Upload </button></li>
            </ul>
            <span class="icon is-left inline md:hidden pr-3"><font-awesome-icon class="" :icon="['fa', 'bars']"> </font-awesome-icon></span>
        </div>
    </div>
</template>
<script>
export default {
    name: "AppNavbar",
    
}


</script>
<style >
  
</style>