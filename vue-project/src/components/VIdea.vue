<script setup>
const idea = [
    {
        class: 'offset-lg-3 col-lg-6 offset-xl-0 col-xl-4 col-xxl-3 idea__cards-first',
        img: {
            src: '/images/lessons.png',
            alt: 'lesson',
        },
        title: 'Составьте расписание',
        description: 'Выберите время, предмет и класс. Ученики получат уведомление о предстоящем уроке.',
    },
    {
        class: 'offset-lg-3 col-lg-6 offset-xl-0 col-xl-4 col-xxl-4 idea__cards-second',
        img: {
            src: '/images/format.png',
            alt: 'format',
        },
        title: 'Подготовьте материал',
        description: 'Загружайте необходимые материалы к уроку.',
    },
    {
        class: 'offset-lg-3 col-lg-6 offset-xl-0 col-xl-4 col-xxl-3 idea__cards-third',
        img: {
            src: '/images/lesson_with_teacher.png',
            alt: 'teacher',
        },
        title: 'Начните урок с учениками',
        description: 'Задавайте вопросы и вызывайте «к доске» детей с поднятой рукой.',
    }
]
</script>

<template>
    <section class="idea">
            <div class="container">
                <div class="idea__wrap">
                    <h6 class="idea__wrap-title">
                        Как это работает?
                    </h6>
                    <div class="row idea__cards">
                        <div v-for="(item, index) in idea"
                            :key="index" :class="item.class"
                            >
                            <img :src="item.img.src" :alt="item.img.alt">
                            <h6>
                                {{ item.title}}
                            </h6>
                            <p>
                                {{ item.description }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
</template>

<style>

</style>