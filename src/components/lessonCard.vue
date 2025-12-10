<template>
    <section class="flex flex-row gap-4 p-4 text-white w-full items-center justify-center">
        <p class="ibm text-[50px] leading-[50px]">{{lCount}}</p>
        <div class="flex flex-col w-full gap-0">
            <p class="inter">{{lName}}</p>
            <div class="flex flex-row gap-2">
                <p>{{lCabinet}}</p>
                <p>{{lTeacher}}</p>
            </div>
        </div>
        <div class="flex flex-col ibm ">
            <p>{{lTime[0]}}</p>
            <p>{{lTime[1]}}</p>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            lTime:[["09:00", "10:30"], ["10:40", "12:10"], ["12:50", "14:20"], ["14:30", "16:00"], ["16:10", "17:40"]][this.lCount - 1],
        }
    },

    props: {
        lCount: {
            type: Number,
            default: 1
        },
        lName : {
            type: String,
            required: true
        },
        lCabinet: {
            type: String,
            required: true
        },
        lTeacher: {
            type: String,
            required: true
        }
    }
}
</script>