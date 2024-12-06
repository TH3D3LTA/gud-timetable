<script setup>
import LessonCard from "./components/LessonCard.vue";
let currentDate = new Date();
let toDay = currentDate.getDate();
let toMonth = currentDate.getMonth();
let toDayWeek = currentDate.getDay();

let days = [
    'вс',
    'пн',
    'вт',
    'ср',
    'чт',
    'пт',
    'сб'
];

let weekEven = [
    'нечётная',
    'чётная'
];

let month = [
    "января",
    "февраля",
    "марта",
    "апреля",
    "мая",
    "июня",
    "июля",
    "августа",
    "сентября",
    "октября",
    "ноября",
    "декабря"
];

let today = new Date(currentDate.getFullYear(), currentDate.getMonth(), 0).getTime();
let now = new Date().getTime();
let week = Math.ceil((now - today) / (1000 * 60 * 60 * 24 * 7));
</script>

<template>
    <section class="flex flex-col bg-gradient-to-b from-black to-white margin-0 h-screen overflow-hidden items-center">
        <div class="flex flex-col py-16 items-center">
            <p class="prata text-white text-[32px] w-fit">{{toDay}} {{month[toMonth]}}, {{days[toDayWeek]}}</p>
            <p class="inter text-white text-[16px] font-regular w-fit">{{weekEven[week]}} неделя</p>
        </div>
        <div class="py-2 bg-[--container-dark] flex flex-col gap-2 text-white h-full p-2 rounded-t-[24px] w-full overflow-y-auto">
            <LessonCard />
            <LessonCard />
            <LessonCard />
            <LessonCard />
        </div>
    </section>
</template>
