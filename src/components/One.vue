<script setup lang="ts">
import { ref, onMounted, nextTick } from 'vue'

const count = ref(0)
const id = 'abc'
const abdDef = 'abcdef'
const html = '<span>111</span>'
const obj = {
    'data-name': 'aaa',
    'data-age': 18
}


async function increment() {
    count.value ++
    await nextTick()
}

onMounted(() => {
    console.log('Component is mounted')
})

</script>

<template>
    <h3>One</h3>
    <button @click.prevent="increment">Count is {{ count }}</button>
    <div v-html="html" :[abdDef]="id" v-bind="obj" :id="id"></div>
</template>

<style scoped>
button {
    font-weight: bold;
}
</style>