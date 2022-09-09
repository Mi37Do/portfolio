<template>
    <div class="h-full w-full flex justify-center items-center py-20">
    <div class="w-full h-full container px-2 lg:px-0  flex flex-col items-center gap-20">
        <div class="w-full  flex flex-col justify-center items-center">
            <span class="text-3xl font-semibold text-gray-700">Portfolio</span>
            <span class="text-lg text-gray-500">Most recent Work</span>
        </div>

        <div class="w-full flex justify-center">
          <div class="w-full h-full hidden xl:grid grid-cols-2 gap-y-10">
            <div class="w-full flex justify-center" v-for="(portfolio, index) in portfolios" :key="index">
                <div class="w-auto flex flex-col lg:flex-row gap-6">
                <img
                    :src="portfolio.source"
                    class="block rounded-md w-[300px] h-[150px] lg:w-[230px] lg:h-[230px] object-cover"
                    alt="Camera"
                />  
                <div class="w-[300px] h-[230px] flex flex-col gap-x-4 gap-y-2 justify-between items-start px-2">
                    <div class="w-full h-auto flex flex-col gap-2">
                       <a class="text-2xl lg:text-xl font-semibold text-gray-700" :href="portfolio.link">{{portfolio.title}}</a>
                       <span class="text-sm text-indigo-500 mb-2">Category : {{portfolio.category}}</span>
                        <p class="text-gray-600 text-sm">{{portfolio.content}}</p> 
                    </div>
                    
                        <a :href="portfolio.link" class="px-4 py-2 bg-indigo-500 rounded text-white">Full Project</a>

                    
                </div>
                </div>
            </div>
        </div>  
        </div>
        
        
        <div id="carouselExampleControls" class="carousel slide relative xl:hidden" data-bs-ride="carousel">
            <div class="carousel-inner relative w-full overflow-hidden">
                <div class="carousel-item relative float-left w-full" v-for="(portfolio, index) in portfolios" :key="index" :class="{'active': index === 0}">
                <div class="w-full flex flex-col lg:flex-row gap-6">
                    <img
                    :src="portfolio.source"
                    class="block rounded-md w-[300px] h-[150px] lg:w-[250px] lg:h-[250px] object-cover"
                    alt="Camera"
                />  
                <div class="w-[300px] h-64 flex flex-col gap-x-4 gap-y-2 justify-between items-start px-2">
                    <div class="w-full h-auto flex flex-col gap-2">
                       <span class="text-2xl font-semibold text-gray-700">{{portfolio.title}}</span>
                       <span class="text-sm text-indigo-500 mb-2">Category : {{portfolio.category}}</span>
                        <p class="text-gray-600 text-sm">{{portfolio.content}}</p> 
                    </div>
                    <div class="w-full flex justify-center">
                       <a :href="portfolio.link" class="px-4 py-2 bg-indigo-500 rounded text-white">Full Project</a> 
                    </div>
                    
                </div>
                    </div>
                </div>
                
                
            </div>
            <button
                class="carousel-control-prev absolute top-0 bottom-0 flex items-center justify-center p-0 text-center border-0 hover:outline-none hover:no-underline focus:outline-none focus:no-underline -left-12 lg:-left-24"
                type="button"
                data-bs-target="#carouselExampleControls"
                data-bs-slide="prev"
            >
                <div class="lg:w-10 lg:h-10 h-7 w-7 bg-indigo-500 rounded-full flex justify-center items-center">
                <UilArrowLeft class="lg:w-7 lg:h-7  w-4 h-4 text-white"/> 
                </div>
            </button>
            <button
                class="carousel-control-next absolute top-0 bottom-0 flex items-center justify-center p-0 text-center border-0 hover:outline-none hover:no-underline focus:outline-none focus:no-underline -right-12 lg:-right-24"
                type="button"
                data-bs-target="#carouselExampleControls"
                data-bs-slide="next"
            >
                <div class="lg:w-10 lg:h-10 h-7 w-7 bg-indigo-500 rounded-full flex justify-center items-center">
                <UilArrowRight class="lg:w-7 lg:h-7  w-4 h-4 text-white"/> 
                </div>
                
                
            </button>
        </div>


    </div>
    </div>
</template>

<script setup>
import { UilArrowRight ,  UilArrowLeft  } from '@iconscout/vue-unicons'
import { ref } from '@vue/reactivity'

const portfolios = ref([
    {
        source:require('@/assets/project01.jpg'),
        title:'Freshka Packaging and Logo Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Freshka", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/145756577/Freshka-Packaging-and-Logo-Design'
    },
    {
        source:require('@/assets/project02.jpg'),
        title:'Congelado Helado Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Pais de Las Maravillas Congelado", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/145676485/Ice-Cream-Brand-Identity'
    },
    {
        source:require('@/assets/pasta01.jpg'),
        title:'La fattoria del sol - packaging design',
        category:'Packaging Design',
        content:'I\'m Glad to Share With You Today One of My Projects "La fattoria del sol", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/139287037/La-fattoria-del-sol-packaging-design'
    },
    {
        source:require('@/assets/travelapp.png'),
        title:'Travel App Website',
        category:'UI/UX Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Pixa.tour", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/144235109/Travel-App-Website'
    },
    {
        source:require('@/assets/all.png'),
        title:'Dahsboard Design',
        category:'UI/UX Design',
        content:'I\'m Glad to Share With You Today One of My Projects Dashboard design, I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/143235469/UI-UX-Task-ManagerDashboard-conception'
    },
    {
        source:require('@/assets/01.png'),
        title:'Gaming Dahsboard Design',
        category:'UI/UX Design',
        content:'I\'m Glad to Share With You Today One of My Projects Gaming Dashboard design, I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/143594303/Gaming-Launcher-Dashboard'
    },
    
    {
        source:require('@/assets/desktop.png'),
        title:'Social Media Design',
        category:'UI/UX Design',
        content:'I\'m Glad to Share With You Today One of My Projects Social Media design, I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/142969293/UI-UX-Social-Media-Website-Design'
    },
    
    {
        source:require('@/assets/nextus.jpg'),
        title:'Nextus Logistics Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Nextus Logistics", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/139490667/Nextus-logistics-brand-identity'
    },
    
    {
        source:require('@/assets/02.png'),
        title:'EL RYADH Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "EL RYADH", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/139233607/EL-RYADH-Brand-Identity'
    },
    {
        source:require('@/assets/04.jpg'),
        title:'Western Beer Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Western Beer", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/138651655/Western-Beer-Brand-Identity'
    },
    {
        source:require('@/assets/bande.jpg'),
        title:'Osaka Food Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Osaka Food", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/137792503/OSAKA-FOOD-Brand-Identity'
    },
    {
        source:require('@/assets/burger.png'),
        title:'Lucifer Burger logo design & food packaging',
        category:'Packaging Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Lucifer Burger", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/137366823/Lucifer-Burger-logo-design-food-packaging'
    },
    {
        source:require('@/assets/divine21.png'),
        title:'Mr Chef Branding Design',
        category:'Branding Design',
        content:'I\'m Glad to Share With You Today One of My Projects "Mr Chef", I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/137376323/Mr-chef-brand-identity'
    },
    {
        source:require('@/assets/apps.png'),
        title:'UI UX Booking App design',
        category:'UI/UX Design',
        content:'I\'m Glad to Share With You Today One of My Projects UI/UX Booking App Design, I\'ll be Happy to See Your Feedbacks',
        link:'https://www.behance.net/gallery/142924505/UI-UX-App-design'
    },
    {
        source:require('@/assets/dogfood.png'),
        title:'CAZANIMO Dog Food packaging design',
        category:'Packaging Design',
        content:'I\'m Glad to Share With You Today One of My Projects "CAZANIMO", I\'ll be Happy to See Your Feedbacks',
        link:'#'
    },
    
    
])
</script>

<style>

</style>