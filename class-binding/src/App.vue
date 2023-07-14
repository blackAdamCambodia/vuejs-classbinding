<script setup>
const bgOrange ='background-color: rgba(251, 146, 60 , 1)'
const bgIndigo = 'background-color: rgba(129,140,248,1)'
const bgGreen = 'background-color: rgba(52,211,153,1)'
 

</script>

<template>
     <section class="container mx-auto">
        <h1 class="text-center text-2xl py-10">Class & Style Binding</h1>

        <section class="flex space-x-10">
            <div class="w-1/3 h-16" :style="bgOrange"></div>
            <div class="w-1/3 h-16" :style="bgGreen"></div>
            <div class="w-1/3 h-16" :style="bgIndigo"></div>
        </section>

        <section class="mt-10 hidden">
            <div class="bg-red-600 h-16 flex items-center justify-center text-white">
                It's a weekday!
            </div>
        </section>

        <section class="mt-10 hidden">
            <div class="bg-teal-100 border-t-4 border-teal-500 rounded-b text-teal-900 px-4 py-3 shadow-md" role="alert">
                <p class="font-bold">Our privacy policy has changed</p>
                <p class="text-sm">Make sure you know how these changes affect you.</p>
            </div>
        </section>
    </section>
   
</template>

<style scoped>

</style>
