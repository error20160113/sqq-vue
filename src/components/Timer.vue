<template>
    <div class="fonts">
        <span>{{iDays}}</span>
        <span>天</span>
        <span>{{iHours}}</span>
        <span>小时</span>
        <span>{{iMinutes}}</span>
        <span>分钟</span>
        <span>{{iSeconds}}</span>
        <span>秒</span>
    </div>

</template>

<script>
    export default {
        name: 'timer',
        data() {
            return {
                beginDate: '2018-10-23 08:30:00',
                iDays: 0,
                iHours: 0,
                iMinutes: 0,
                iSeconds: 0,

            };
        },
        methods: {
            dateDiff() {
                var date2 = new Date();
                var date1 = new Date(Date.parse(this.beginDate.replace(/-/g, "/")));
                var milliseconds = Math.abs(date2.getTime() - date1.getTime());
                this.iDays = parseInt(milliseconds / 1000 / 60 / 60 / 24);
                this.iHours = parseInt((milliseconds - (this.iDays * 1000 * 60 * 60 * 24)) / 1000 / 60 / 60);
                this.iMinutes = parseInt((milliseconds - (this.iDays * 1000 * 60 * 60 * 24) - (this.iHours * 1000 * 60 *
                    60)) / 1000 / 60);
                this.iSeconds = parseInt((milliseconds - (this.iDays * 1000 * 60 * 60 * 24) - (this.iHours * 1000 * 60 *
                    60) - (this.iMinutes * 1000 * 60)) / 1000);

            },
        },
        mounted() {
            this.dateDiff();
        },
    }
</script>

<style scoped>
    .fonts {
        font-size: larger;
        color: royalblue;
        height: 50%;
    }
</style>