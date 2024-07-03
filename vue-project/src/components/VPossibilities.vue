<script setup>
const possibilities = [
    {
        /*class: 'col-lg-4 col-xl-3 possibilities__cards-card possibilities__cards-first',*/
        class: 'possibilities__cards-card possibilities__cards-first',
        img: {
            src: '/images/chat.png',
            alt: 'chat',
        },
        title: 'Общение с классом',
        description: 'Видеосвязь Чат с классом',
    },
    {
        /*class: 'offset-lg-1 col-lg-4 offset-xl-0 col-xl-3 possibilities__cards-card possibilities__cards-second',*/
        class: 'possibilities__cards-card possibilities__cards-second',
        img: {
            src: '/images/computer.png',
            alt: 'computer',
        },
        title: 'Проведение занятий',
        description: 'Презентация файлов Демонстрация экрана',
    },
    {
        /*class: 'col-lg-4 col-xl-3 possibilities__cards-card possibilities__cards-third',*/
        class: 'possibilities__cards-card possibilities__cards-third',
        img: {
            src: '/images/marks.png',
            alt: 'marks',
        },
        title: 'Посещаемость',
        description: 'Автоматическое отслеживание присутствующих',
    },
    {
        /*class: 'offset-lg-1 col-lg-4 offset-xl-0 col-xl-3 possibilities__cards-card possibilities__cards-fourth',*/
        class: 'possibilities__cards-card possibilities__cards-fourth',
        img: {
            src: '/images/reset.png',
            alt: 'chat',
        },
        title: 'История занятий',
        description: 'Материалы урока',
    }
]
import Swiper from "swiper";
import { onMounted } from "vue";
import {Navigation, Pagination} from "swiper/modules";

onMounted(() => {
    const swiper = new Swiper(".mySwiper", {
                    modules: [Pagination, Navigation],
                    loop: true,
                    slidesPerView: 4,
                    spaceBetween: 30,
                    pagination: {
                        el: ".swiper-pagination",
                    },
                    mousewhell: true,
                    keyboard: true,
                    breakpoints: {
                        0: {
                            slidesPerView: 1,
                        },
                        576: {
                            slidesPerView: 2,
                        },
                        992: {
                            slidesPerView: 4,
                        },
                    },
                });
})
</script>

<template>
    <section class="possibilities">
            <div class="container">
                <div class="possibilities__wrap">
                    <h4>
                        Возможности
                    </h4>
                    <div class="possibilities__cards">
                        <div class="swiper mySwiper">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide"  
                                    v-for="(item, index) in possibilities"
                                    :key="index"
                                    >
                                    <div :class="item.class">
                                    <img :src="item.img.src" :alt="item.img.alt">
                                    <h5>
                                        {{item.title}}
                                    </h5>
                                    <p>
                                        {{item.description}}
                                    </p>
                                    </div> 
                                </div>
                            </div>
                            <div class="swiper-pagination"></div>
                        </div>
                    </div>
                </div>
            </div>
            
        </section>
</template>

<style>

</style>