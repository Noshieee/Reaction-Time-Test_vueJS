<template>
  <p>Reaction time - {{ score }} ms</p>
</template>

<script>
export default {
    props:['score'],
    data() {
        return {
            rank:null
        }
    },
    mounted() {
        if (this.score < 290) {
            this.rank = 'Ninja Fingers'
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflexes'
        } else {
            this.rank = 'Snail Pace...'
        }
    },
}
</script>

<style>
    .rank{
        font-size: 1.4rem;
        color: purple;
        font-weight: bold;
    }
</style>