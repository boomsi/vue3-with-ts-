<script lang="ts">
import { ref } from 'vue';


export default {
    setup() {
        const count = ref(0)

        function increment() {
            count.value ++
        }

        return {count, increment}
    }
}

</script>

<template>
    <h3>Two</h3>
    <button @click="increment">{{ count }}</button>
</template>