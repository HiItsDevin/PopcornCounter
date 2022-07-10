<script setup>
import { ref } from 'vue'

const popcornBucketsEaten = ref(0)
</script>

<template lang="pug">
div
    p.popcorn(onclick="alert('uh, this isnt the popcorn youre trying to actually eat, i hope you know that.')")
    h1.pleaseJustCenterText trying to eat some fucking popcorn while watching this bullshit unfold
    h2.pleaseJustCenterText buckets of popcorn eaten: {{popcornBucketsEaten}}
    it-button.theFunnyButton.pulse(type="warning" @click="popcornBucketsEaten++") 🍿

</template>

<style scoped>
div {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.pleaseJustCenterText {
    text-align: center;
}

.theFunnyButton {
    position: fixed;
    left: 50%;
    transform: translate(-50%, 100%);

}

.popcorn {
    margin-top: -128px;
    text-align: center;
}

.popcorn::after {
    content: "\1F37F";
    font-size: 256px;
}
</style>