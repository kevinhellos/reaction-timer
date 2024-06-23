<template>
    <h1 class="rank"> {{ rank }} </h1>
    <p>Reaction time {{ score }} ms</p>
</template>

<script>
export default {
    props: ["score"],
    data() {
        return {
            rank: null
        }
    },

    mounted() {
        if (this.score < 250) {
            this.rank = "🥷 Ninja Fingers";
        } 
        else if (this.score < 400) {
            this.rank = "⚡ Rapid Reflexes";
        }
        else {
            this.rank = "🐌 Snail pace";
        }
    }
}
</script>

<style>

</style>