<script setup>
const work = [
    {
        img:{
            src: '/table.svg',
            alt: 'Составьте расписание',
        },
        name:'Составьте расписание',
        text:['Выберите время, предмет и класс.', 'Ученики получат уведомление о', 'предстоящем уроке.']
    },
    {
        img:{
            src: '/materIAL.svg',
            alt: 'Подготовьте материал',
        },
        name:'Подготовьте материал',
        text:['Загружайте необходимые материалы', 'к уроку.']
    },
    {
        img:{
            src: '/start_lesson.svg',
            alt: 'Начните урок с учениками',
        },
        name:'Начните урок с учениками',
        text:['Задавайте вопросы и вызывайте', '«к доске» детей с поднятой рукой.']
    }
]

</script>

<template>
<section class="work">
            <div class="container">
                <h2>Как это работает?</h2>
                <div class="row">
                    <div class="col-12 col-sm-6 col-lg-4" 
                        v-for="(item, index) in work"
                        :key="index"
                    >
                        <div class="work__card">
                            <img :src="item.img.src" :alt="item.img.alt">
                            <div class="work__card-name">
                                {{ item.name }}
                            </div>
                            <p v-for="(item,index) in item.text"
                                :key="index">
                                {{ item}}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
</template>

<style scoped>

</style> 