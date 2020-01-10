<template>
    <div class="fonts">
        <span>{{iDays}}天</span>
    </div>

</template>

<script>
    export default {
        name: 'timer',
        data() {
            return {
                beginDate: '2018-10-23 00:00:01',
                iDays: 0,
            };
        },
        methods: {
            dateDiff() {
                var date2 = new Date();
                var date1 = new Date(Date.parse(this.beginDate.replace(/-/g, "/")));
                var milliseconds = Math.abs(date2.getTime() - date1.getTime());
                this.iDays = parseInt(milliseconds / 1000 / 60 / 60 / 24);
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