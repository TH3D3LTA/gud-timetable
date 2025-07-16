<template>
    <section class="flex flex-row gap-4 p-4 text-white w-full items-center justify-center">
        <p class="ibm text-[50px] leading-[50px]">{{this.lessonCount}}</p>
        <div class="flex flex-col w-full gap-0">
            <p class="inter">Math analyze</p>
            <div class="flex flex-row gap-2">
                <p>1-118</p>
                <p>Grishanina G.E.</p>
            </div>
        </div>
        <div class="flex flex-col ibm ">
            <p>09:00</p>
            <p>10:30</p>
        </div>
    </section>
</template>

<script>
import info from `../src/timetable.json`;

export default {
    props: {
        lessonCount: {
            type: Number,
            default: 1
        }
    }
}
</script>