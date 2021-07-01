<template>
    <p>Reaction time : {{ score }} ms.</p>
    <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = "Like a freakin' ninja my dude"
        } else if (this.score < 400) {
            this.rank = "Rapid flexes bro"
        } else {
            this.rank = ".. bruh, u a snail"
        }
    }
}
</script>

<style>
.rank {
    font-size: 1.4em;
    color: orangered;
    font-weight: bold;
}
</style>