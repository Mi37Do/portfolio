<template>
    <div class="h-full w-full flex justify-center items-center py-20">
    <div class="w-full h-full container px-2 lg:px-0  flex flex-col items-center gap-20">
        <div class="w-full  flex flex-col justify-center items-center">
            <span class="text-3xl font-semibold text-gray-700">Contact Me</span>
            <span class="text-lg text-gray-500">Get in touch</span>
        </div>
        <div class="w-full h-full grid grid-cols lg:grid-cols-2 gap-y-8">
            <div class="w-full h-auto flex flex-col gap-12 items-center">
                <div class="w-auto h-auto flex gap-4 items-center" v-for="contact in contacts" :key="contact">
                    <div class="w-10 h-10 flex-none">
                        <UilPhoneAlt v-if="contact.title === 'Phone Number'" class="h-full w-full text-indigo-500"/>
                        <UilEnvelope v-if="contact.title === 'Email'" class="h-full w-full text-indigo-500"/>
                        <UilLocationPoint v-if="contact.title === 'Location'" class="h-full w-full text-indigo-500"/>
                    </div>
                    <a class="w-[270px] h-full flex flex-col" :href="contact.link">
                        <span class="text-gray-700 text-lg font-medium">{{contact.title}}</span>
                        <a class="text-gray-500 text-md " :href="contact.link">{{contact.data}}</a>
                    </a>
                </div>
            </div>
            <div class="w-full h-auto flex flex-col gap-6 items-center">
                <div class="w-full flex flex-col gap-2 items-center lg:items-start justify-start">
                    <div class="w-full flex items-start">
                       <span class="text-lg text-gray-700">Name</span> 
                    </div>
                    
                    <input type="text" class="w-full lg:w-96 h-14 border-2 rounded-md focus:outline-indigo-500 px-4"/>
                </div>
                <div class="w-full flex flex-col gap-2 items-center lg:items-start justify-start">
                    <div class="w-full flex items-start">
                       <span class="text-lg text-gray-700">Email</span> 
                    </div>
                    
                    <input type="email" class="w-full lg:w-96 h-14 border-2 rounded-md focus:outline-indigo-500 px-4"/>
                </div>
                <div class="w-full flex flex-col gap-2 items-center lg:items-start justify-start">
                    <div class="w-full flex items-start">
                       <span class="text-lg text-gray-700">Project</span> 
                    </div>
                    
                    <input type="text" class="w-full lg:w-96 h-14 border-2 rounded-md focus:outline-indigo-500 px-4"/>
                </div>
                <div class="w-full flex flex-col gap-2 items-center lg:items-start justify-start">
                    <div class="w-full flex items-start">
                       <span class="text-lg text-gray-700">Message</span> 
                    </div>
                    
                    <textarea type="text" class="w-full lg:w-96 border-2 rounded-md focus:outline-indigo-500 p-4"/>
                </div>
                <div class="w-full flex justify-center lg:justify-start">
                  <button class="bg-indigo-500 flex py-3 px-6 rounded-md text-white gap-6 items-center">Send Message <UilMessage class="w-5 h-5"/></button>  
                </div>
                
            </div>
        </div>
    </div>
    </div>
</template>
        
<script setup>
import { UilPhoneAlt , UilEnvelope ,UilLocationPoint ,UilMessage } from '@iconscout/vue-unicons'
const { ref }=require("@vue/reactivity");


const contacts = ref([
{
title :'Phone Number',
data:'(+213) 057-78-56-77',
link:'#contact'
},
{
title :'Email',
data:'mido37mido37@gmail.com',
link:'#contact'
},
{
title :'Location',
data:'Sidi Bel Abbes - ALGERIA',
link:'https://goo.gl/maps/7bgSnumcdPhYrTnWA'
},
])
</script>
        
<style>
        
</style>