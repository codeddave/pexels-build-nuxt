<template lang="">
    <div class="hero px-4 md:px-0">
        <div class="flex flex-col justify-center items-center">
        <div class="text-white pt:8 md:pt-40  max-w-2xl mx-auto font-bold hero-content"> 
            <h1 class="text-4xl">The best free stock photos and videos shared by talented creators.</h1>
            <input class="w-full h-14 mt-8 pl-4 text-lg outline-none text-gray-600 rounded" placeholder="Search for free photos and videos"/>
            <p class="text-left pl-0 max-w-2xl">Suggested: <span class="text-xs font-normal ">trees  sky  forest  white background  branch  flowers  more</span></p>
        </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "Hero"
}
</script>
<style>
    .hero {
        background-image: url("../assets/hero-image.jpg");
        background-position: center;
        background-size: cover;
        filter: brightness(90%);

        width: 100%;
        height: 500px;
    }
</style>