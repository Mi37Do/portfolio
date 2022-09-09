<template>
  <div class="w-full h-[85vh]  flex flex-col-reverse lg:flex-row gap-2 lg:gap-4">
    <div class="w-full h-full  flex flex-row gap-20 items-center justify-center">
      <div class="w-16 h-full hidden lg:flex flex-col items-end justify-center gap-6 text-indigo-500">
        <a class="w-8 h-8 " href="https://www.linkedin.com/in/salah-eddine-laksari/">
          <UilLinkedinAlt class="w-full h-full"/>
        </a>
        <a class="w-8 h-8 " href="https://www.behance.net/midolaksari">
          <UilBehance class="w-full h-full"/>
        </a>
        <a class="w-8 h-8 " href="https://dribbble.com/laksari">
          <UilDribbble class="w-full h-full"/>
        </a>
      </div>
      <div class="w-full h-full flex flex-col justify-center items-center lg:items-start gap-4 text-center lg:text-left">
        <span class="text-2xl lg:text-3xl font-bold text-indigo-500">Hi, I'm Salah Eddine LAKSARI</span>
        <span class="text-gray-600 text-lg lg:text-xl font-medium">UI/UX Designer <span class="text-indigo-500">&</span> Front-end Developer</span>
        <p class="text-gray-500 text-sm mb-2">High level experience in web design and developement knowledge, producing work</p>
        <a class="bg-indigo-500 flex py-3 px-6 rounded-md text-white gap-6 items-center" href="#contact">Contact Me <UilMessage class="w-5 h-5"/></a>
      </div>
    </div>
    
    <div class="w-full h-auto flex items-center justify-center  gap-2 pt-20 lg:pt-0">

        <div class="w-16 h-full flex lg:hidden flex-col items-center justify-center gap-6 text-indigo-500">
        <a class="w-6 h-6">
          <UilLinkedinAlt class="w-full h-full" href="https://www.linkedin.com/in/salah-eddine-laksari/"/>
        </a>
        <a class="w-6 h-6" href="https://www.behance.net/midolaksari">
          <UilBehance class="w-full h-full"/>
        </a>
        <a class="w-6 h-6"  href="https://dribbble.com/laksari">
          <UilDribbble class="w-full h-full"/>
        </a>
      </div>

    <img src="@/assets/mepng.png" class="w-[300px] lg:w-[500px]" alt="">


    </div>
  </div>
</template>

<script setup>
import { UilLinkedinAlt , UilBehance , UilDribbble ,  UilMessage } from '@iconscout/vue-unicons'
</script>

<style>

</style>