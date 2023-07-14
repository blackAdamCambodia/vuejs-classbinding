<script setup>
// you can write all css properties as you write in style file and bind , 
const bgOrange ='background-color: rgba(251, 146, 60 , 1); font-size:24px; color:red'
const bgIndigo = 'background-color: rgba(129,140,248,1)'
const bgGreen = 'background-color: rgba(52,211,153,1)'
const textColor ='color:white'

const weekend = false;
const bgRed = 'background-color: rgb(220,38,38)'
const bgDarkGreen= 'background-color: rgb(5,150,105)'

const colors= {
    borderColor: 'rgba(20,184,166,1)',
    color: 'rgba(19,78,74,1)',
    backgroundColor: 'rgba(204,251,241,1)'
}

const messageType= 'error' ;

if ('error' == messageType){
    colors.borderColor= 'rgba(239,68,68,1)',
    colors.color = 'rgba(254,226,226,1)',
    colors.backgroundColor = 'rgba( 127,29, 29,1)'
}
 
if ('warning' == messageType){
  colors.borderColor = 'rgba( 122,244,61,1)',
  colors.color = 'rgba(18,91,51,1)',
  colors.backgroundColor='rgba(100,200,51)'
}

</script>

<template>
     <section class="container mx-auto">
        <h1 class="text-center text-2xl py-10">Style Binding</h1>
        <h4>What is the difference between Class and style binding</h4>
        <p class="my-5 bg-slate-200 text-red-700">In style we write the properties and value in a variable the bind the :style and call the variable . For example : const bgOrange ='background-color: rgba(251, 146, 60 , 1); font-size:24px; color:red'</p>
        <section class="flex space-x-10">
            <div class="w-1/3 h-16" :style="bgOrange">many style binding</div>
            <!-- you can bind many variable in one style as a array -->
            <div class="w-1/3 h-16" :style="[bgGreen,textColor]">style properties bind as a array</div>
            <div class="w-1/3 h-16" :style="bgIndigo"></div>
        </section>

        <section class="mt-10">
            <p class="my-5 bg-slate-200 text-red-700">Conditionally bind the css style </p>
            <div class="h-16 flex items-center justify-center text-white" :style="weekend== true ? bgRed : bgDarkGreen">
                It's a weekday!
            </div>
        </section>

        <section class="mt-10">
            <div class=" border-t-4  rounded-b  px-4 py-3 shadow-md" :style="colors">
                <p class="font-bold">Our privacy policy has changed</p>
                <p class="text-sm">Make sure you know how these changes affect you.</p>
            </div>
        </section>
    </section>
   
</template>

<style scoped>

</style>
