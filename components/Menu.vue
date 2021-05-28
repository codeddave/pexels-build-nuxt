<template lang="">
    <div class="flex justify-center shadow overflow-x-scroll md:overflow-x-hidden">
        <div class=""> 
            <ul class="list-none flex py-2 md:py-6 text-gray-600 text-base md:text-lg  font-normal">
                <li class="pl-12 hover:text-blue-700 hover:font-bold font-normal ">Home</li>   
                <li class="pl-12 hover:text-blue-700 hover:font-bold">Discover</li>    
                <li class="pl-12 hover:text-blue-700 hover:font-bold">Videos</li>    
                <li class="pl-12 hover:text-blue-700 hover:font-bold">Leaderboard</li>    
                <li class="pl-12 hover:text-blue-700 hover:font-bold">Challenges</li>    
            </ul> 
        </div>   
    </div>
</template>
<script>
export default {
    name: "Menu",

    head() {
        return {
            title: "Menu"
        }
    }
}
</script>
<style lang="">
    
</style>