<template>

  
  <header class="w-full h-16 bg-white sticky z-20 top-0 left-0 hidden justify-center items-center lg:flex   bg-clip-padding blur-backdrop-filter bg-blur-lg bg-opacity-80">
    <nav class="container w-full h-full px-8 flex justify-between items-center">
      <a href="#" class="text-lg font-semibold text-gray-700">pixa<span class="text-indigo-500">viz.</span></a>
      <div class="w-full h-full flex justify-end items-center gap-6 text-indigo-500 text-sm">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Portfolio</a>
        <button class="w-auto h-auto py-2 px-4 bg-indigo-500 rounded text-white">
          <a href="#contact">Contact Me</a>
        </button>
        
      </div>
    </nav>
  </header>
  
  <div class="w-full h-full flex justify-center items-center bg-white">
    
    <div class="w-full h-full container bg-white flex flex-col">
      <section class="w-full h-full px-8" id="home">
        <Home/>
      </section>
      <section class="w-full h-auto px-8" id="about">
        <About/>
      </section>
      <section class="w-full h-full px-8" id="skills">
        <Skills/>
      </section>
      <section class="w-full h-full px-8">
        <Qualification/>
      </section>
      <section class="w-full h-full px-8" id="services">
        <Services/>
      </section>
      <section class="w-full h-full px-8" id="portfolio">
        <Portfolio/>
      </section>
      <section class="w-full h-full px-8" id="contact">
        <Contactme/>
      </section>
      <section class="w-full h-full px-8">
        <Footer/>
      </section>
    </div>
  </div>
  <div class="w-screen h-screen fixed z-10 inset-0" :class="{'invisible' : !bottomMenu, 'visible' : bottomMenu}">
    <div class="w-full h-full bg-gray-700 opacity-80 absolute z-10 inset-0 ease-in transition-all overflow-x-hidden overflow-y-auto duration-500" :class="{'opacity-0' : !bottomMenu, 'opacity-80' : bottomMenu}" @click="openMenu"></div>
    <div class="w-full h-64 bg-white fixed bottom-0 left-0 z-10 transition-all duration-1000 rounded-t-xl p-4" :class="{'translate-y-full h-64' : !bottomMenu , 'translate-y-0 h-16 mb-16': bottomMenu}">
      <div class="w-full h-full grid grid-cols-3 text-indigo-500">
        <a class="w-full h-full flex flex-col justify-center items-center gap-2"   href="#home">
          <UilEstate class="w-6 h-6" />
          <span class="text-sm font-medium">Home</span>
        </a>
        <a class="w-full h-full flex flex-col justify-center items-center gap-2"  href="#about">
          <UilUser class="w-6 h-6" />
          <span class="text-sm font-medium">About</span>
        </a>
        <a class="w-full h-full  flex flex-col justify-center items-center gap-2"   href="#skills">
          <UilFileAlt class="w-6 h-6" />
          <span class="text-sm font-medium">Skills</span>
        </a>
        <a class="w-full h-full  flex flex-col justify-center items-center gap-2" href="#services">
          <UilBriefcaseAlt class="w-6 h-6" />
          <span class="text-sm font-medium">Services</span>
        </a>
        <a class="w-full h-full  flex flex-col justify-center items-center gap-2" href="#portfolio">
          <UilScenery class="w-6 h-6" />
          <span class="text-sm font-medium">Portfolio</span>
        </a>
        <a class="w-full h-full  flex flex-col justify-center items-center gap-2" href="#contact">
          <UilMessage class="w-6 h-6" />
          <span class="text-sm font-medium">Contact me</span>
        </a>
      </div>
    </div>
  </div>

  <div class="w-full h-16 sticky z-20 bottom-0 bg-white left-0 flex items-center justify-between px-4 lg:hidden">
    <a href="#" class="text-lg font-bold text-gray-800">pixa<span class="text-indigo-500">viz.</span></a>
    <button @click="openMenu" class="w-8 h-8 flex items-center justify-center">
      <UilApps class="w-6 h-6 text-indigo-500"/>
    </button>
  </div>
  <!--
  
  -->
</template>

<script setup>
import Home from '@/components/Home.vue'
import About from '@/components/About.vue'
import Skills from '@/components/Skills.vue'
import Qualification from '@/components/Qualification.vue'
import Services from '@/components/Services.vue'
import Portfolio from '@/components/Portfolio.vue'
import Contactme from '@/components/Contactme.vue'
import Footer from '@/components/Footer.vue'
import { UilApps ,  UilEstate , UilUser , UilFileAlt ,UilBriefcaseAlt ,UilScenery ,UilMessage } from '@iconscout/vue-unicons'
const { ref }=require("@vue/reactivity");

const bottomMenu = ref(false)
function openMenu(){
  if(bottomMenu.value === false){
    bottomMenu.value = true
    
  }
  else bottomMenu.value = false
  console.log(bottomMenu.value);
}
</script>



<style lang="scss">
html {
  scroll-behavior: smooth;
}
#app {
  font-family: 'Poppins', sans-serif;
}
.blur-backdrop-filter{
  backdrop-filter: blur(6px);
  --webkit-backdrop-filter: blur(5px)
}
</style>
