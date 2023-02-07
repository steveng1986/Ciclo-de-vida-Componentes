<template>
    <div>{{ text }}</div>
    <div>{{ counter }}</div>

</template>

<script>
import { ref, watch } from "vue"
export default {
    setup() {
        const text = ref("new class");
        const counter = ref(0);
        setInterval(() => counter.value++, 1000)
        watch(counter, (valor, anterior) => {
            console.log(valor, anterior);
        } )
        return {
            text,
            counter,
        }
    },
    }
</script>
