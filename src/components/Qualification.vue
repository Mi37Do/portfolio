<template>
  <div class="w-full h-full flex flex-col gap-6 items-center py-20">
    <div class="w-full  flex flex-col justify-center items-center">
            <span class="text-3xl font-semibold text-gray-700">Qualification</span>
            <span class="text-lg text-gray-500">My personal journey</span>
        </div>
            <div class="w-full lg:w-96 h-16 rounded-md bg-gray-100 flex p-2 gap-2">
                <div class="w-1/2 h-12 flex rounded  items-center justify-center gap-2  transition-all duration-1000" :class="{'bg-indigo-500 text-white' : qualificationShow === 'education', 'text-indigo-500' : qualificationShow === 'work'}" @click="qualificationShowing('education')">
                    <UilGraduationCap class="w-5 h-5"/>
                    <span class="text-sm font-medium cursor-pointer">Education</span>
                </div>
                <div class="w-1/2 h-12 flex rounded items-center justify-center gap-2  transition-all duration-1000" :class="{'bg-indigo-500 text-white' : qualificationShow === 'work', 'text-indigo-500' : qualificationShow === 'education'}" @click="qualificationShowing('work')">
                    <UilBriefcaseAlt class="w-5 h-5"/>
                    <span class="text-sm font-medium cursor-pointer">Experience</span>
                </div>
                
            </div>
            <QualificationCard :qualificationShow="{qualificationShow}"/>
        </div>
</template>

<script setup>
import { UilGraduationCap ,  UilBriefcaseAlt } from '@iconscout/vue-unicons'
import QualificationCard from './QualificationCard.vue'
const { ref }=require("@vue/reactivity");


const qualificationShow = ref('education')
function qualificationShowing(e){
    if (e === 'education'){
        qualificationShow.value = 'education'
    }
    else{
        qualificationShow.value = 'work'
    }
}

</script>

<style>

</style>