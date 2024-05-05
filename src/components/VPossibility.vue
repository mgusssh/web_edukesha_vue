<script setup>


const possibility = [
    {
        img:{
            src: '/communication.svg',
            alt: 'Общение с классом',
        },
        name: 'Общение с классом',
        text: ['Видеосвязь', 'Чат с классом']
    },
    {
        img:{
            src: '/lessons.svg',
            alt: 'Проведение занятий',
        },
        name: 'Проведение занятий',
        text: ['Презентация файлов', 'Демонстрация экрана']
    },

    {
        img:{
            src: '/attendance.svg',
            alt: 'Посещаемость',
        },
        name: 'Посещаемость',
        text: ['Автоматическое', 'отслеживание ', 'присутствующих']
    },
    {
        img:{
            src: 'history.svg',
            alt: 'История занятий',
        },
        name: 'История занятий',
        text: ['Материалы урока']
    },
]

import Swiper from 'swiper';
import { onMounted } from 'vue'
import {Navigation, Pagination} from "swiper/modules";

onMounted(() => {
    window.swiper = new Swiper(".mySwiper", {
    modules: [Navigation, Pagination],
    spaceBetween: 10,
    pagination: {
      el: ".swiper-pagination",
    },
    mousewheel: true, 
    slidesPerView: 1,
    breakpoints: {
        640: {
          slidesPerView: 2,
          spaceBetween: 20,
        },
        768: {
          slidesPerView: 3,
          spaceBetween: 20,
        },
        1024: {
            slidesPerView: 4,
            spaceBetween: 20,
        },
    }
  });

});




</script>

<template>
<section class="possibility">
            <div class="container">
                <h2>
                    Возможности
                </h2>
                <div class="swiper mySwiper">
                    <div class="swiper-wrapper">

                        <div class="swiper-slide" 
                            v-for="(item, index) in possibility"
                            :key="index">   
                            <div :class="`possibility__card card-${index}`">
                                <img :src="item.img.src" :alt="item.img.alt">
                                <div class="possibility__card-name">
                                        {{ item.name }}
                                </div>
                                <p v-for="(item, index) in item.text"
                                    :key="index">
                                    {{ item }}
                                </p>
                            </div>  
                        </div>

                    </div>
                    <div class="swiper-pagination"></div>
                </div>
            </div>
        </section>
</template>

<style scoped>

</style> 