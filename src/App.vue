<template>
    <section class="flex flex-col bg-gradient-to-b from-black to-white margin-0 h-screen overflow-hidden items-center">
        <div class="flex flex-col py-16 items-center justify-center h-full">
            <p class="prata text-white text-[32px] w-fit">{{this.toDate}} {{this.toMonth}}, {{this.toWeekDay}}</p>
            <p class="inter text-white text-[16px] font-regular w-fit">{{isEvenWeek}} week</p>
        </div>
        <div class="flex p-1 flex-col h-fit bg-black w-full">
            <lesson-card l-count="1" l-name="Math analyze" l-cabinet="1-100" l-teacher="Senner A.E." />
            <lesson-card l-count="2" l-name="Math analyze" l-cabinet="1-100" l-teacher="Senner A.E." />
            <lesson-card l-count="3" l-name="Math analyze" l-cabinet="1-100" l-teacher="Senner A.E." />
            <lesson-card l-count="4" l-name="Math analyze" l-cabinet="1-100" l-teacher="Senner A.E." />
        </div>
    </section>
</template>

<script>
import LessonCard from "@/components/lessonCard.vue";

export default {
    name: 'App',
    components: {LessonCard},
    data() {
        return {
            toDate: new Date().getDate(),
            toMonth: ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"][new Date().getMonth()],
            toWeekDay: ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"][new Date().getDay()],
            isEvenWeek: ["Even", "Odd"][Math.floor(new Date() / 60480000) % 2],
        }
    }
}
</script>