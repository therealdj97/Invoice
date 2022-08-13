<template>
    <section class="mt-5"> 
        <div>
            <!-- <img src="../static/favicon.ico"> -->
        </div>
        <div>
            <!-- <h2>{{ today }}</h2> -->
            <h1 class="text-4xl font-bold text-center">Invoice</h1>
            <!-- <h2 class="count++">{{ count }}</h2> -->
        </div>
    </section>
</template>
    <script>
export default {
    data() {
        return {
            count: "",
        }
    },
    methods: {
        today() {

            const weekday = [
                "Sunday",
                "Monday",
                "Tuesday",
                "Wednesday",
                "Thursday",
                "Friday",
                "Saturday"
            ];
            const current = new Date();
            // const date = (current.getMonth() ) + current.getFullYear() + current.getDate();
            const date = current.getFullYear();
            const time =
                current.getHours() +
                ":" +
                current.getMinutes() +
                ":" +
                current.getSeconds();
            const year = current.getFullYear();
            const month = current.getMonth();
            // const week = current.getDay();
            const d = new Date();
            var day = weekday[d.getDay()];
            const dateTime = year + " " + " " + day;
            const yearMonth = year + " " + month;
            return dateTime;
        }
    }
}
</script>