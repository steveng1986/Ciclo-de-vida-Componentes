<template>
    <div>{{ text }}</div>
    <div>{{ counter }}</div>

</template>

<script>
import { ref } from "vue"
export default {
    setup() {
        const text = ref("new class");
        const counter = ref(0);
        setInterval(() => counter.value++, 500);

        return {
            text,
            counter,
        }
    },
    }
</script>
