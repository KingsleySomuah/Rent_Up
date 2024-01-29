<template>
<div>
    <div class="flex justify-between container p-4 items-center">
        <div class="flex items-center">
            <p class="font-bold text-gray-700 text-2xl">Rent</p>
            <span class="font-medium text-green-600 text-2xl">UP</span>
        </div>
        <nav class="md:flex hidden">
            <ul class="flex gap-3">
                <RouterLink to="/">
                    <li>Home</li>
                </RouterLink>
                <RouterLink to="/about">
                    <li>About</li>
                </RouterLink>
                <RouterLink to="/services">
                    <li>Service</li>
                </RouterLink>
                <RouterLink to="/blog">
                    <li>Blog</li>
                </RouterLink>
                <RouterLink to="/pricing">
                    <li>Pricing</li>
                </RouterLink>
                <RouterLink to="/contact">
                    <li>Contact</li>
                </RouterLink>
            </ul>
        </nav>
        <div class="md:flex items-center gap-3 hidden">
        <button class="flex items-center gap-1">
            <div class="w-6 h-6 flex justify-center items-center p-2 rounded-full bg-green-600">
                <p class="text-white font-medium">2</p>
            </div>
            My list</button>
        <button class="bg-green-600 px-3 py-2 w-100 text-white rounded-lg">Sign-In</button>
       
    </div>
        <div class="flex md:hidden" @click="toggleNav">
                <img src="../../assets/icons/bars-solid.svg" alt="" width="20">
            </div>
            <div class=" md:hidden fixed" :class="showNav?'fixed block top-0 right-0 w-full bg-black/50 h-screen left-0' : 'hidden right-[-100%]' ">
                <div class="p-8 bg-white">
                    <img src="../../assets/icons/xmark-solid.svg" alt="" width="20" @click="toggleNav">
                </div>
            </div>
    </div>
</div>
    

</template>

<script setup>
    let showNav=false
    function toggleNav(){
        showNav=!showNav
        console.log(showNav)
    }
</script>

<style scoped>

</style>