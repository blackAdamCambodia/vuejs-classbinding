<script setup>
// in Class we use the value in variable in and bind the variable in vue js . in style we use properties and value in variable then bind in vue js. here we show how to bind the class
const bgOrange ='bg-orange-400'
const bgIndigo = 'bg-indigo-400'
const bgGreen = 'bg-green-400'
 const textColor ='text-white'

const weekday = false;
const bgRed = 'rgb(220,38,38)'
const bgDarkGreen= ' bg-green-600'

const colors= {
    borderColor: 'border-green-400',
    color: 'text-teal-900',
    bgColor: 'bg-teal-100'
}


const messageType = 'warning'

if('error'==messageType){
  colors.bgColor = 'bg-red-100'
  colors.borderColor = 'border-red-500'
  colors.textColor = 'text-red-900'
}

if('warning'==messageType){
  colors.bgColor = 'bg-orange-100'
  colors.borderColor = 'border-orange-500'
  colors.textColor = 'text-orange-900'
}
</script>

<template>
     <section class="container mx-auto">
        <h1 class="text-center text-2xl py-10">Class Binding</h1>
        <h4>Here we show how to bind class in vue js</h4>
        <p class="my-5 bg-slate-200 text-red-700">in Class we use the value in variable in and bind the variable in vue js. For example : const bgOrange ='bg-orange-400' now bind this class in vue js</p>
        <section class="flex space-x-10">
            <div class="w-1/3 h-16" :class="bgOrange"></div>
            <!-- you can bind many variable in one class as a array -->
            <div class="w-1/3 h-16" :class="[bgGreen,textColor]">many class variable bind as a array in class</div>
            <div class="w-1/3 h-16" :class="bgIndigo"></div>
        </section>

        <section class="mt-10">
            <p class="my-5 bg-slate-200 text-red-700">Conditionally bind the css value in class.when you write variable name don't use ''  </p>
            <div class="h-16 flex items-center justify-center text-white" :class="[weekday== true ? bgRed : bgDarkGreen]">
                It's a weekday!
            </div>
        </section>

        <section class="mt-10">
            <div class=" border-t-4  rounded-b  px-4 py-3 shadow-md" :class="[colors.borderColor, 'colors.textColor', colors.bgColor]">
                <p class="font-bold">Our privacy policy has changed</p>
                <p class="text-sm">Make sure you know how these changes affect you.</p>
            </div>
        </section>
    </section>
   
</template>

<style scoped>

</style>
