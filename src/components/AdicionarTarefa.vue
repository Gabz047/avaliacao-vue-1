<script setup>
import {ref, reactive} from 'vue'
const model = ref('')

const emits = defineEmits([
    'adicionarTarefa'
])

</script>

<template>
    <section>
        <h2>Adicione uma nova tarefa</h2>
        <input type="text" v-model="model" />
        <button @click="emits('adicionarTarefa')">Adicionar</button>
    </section>
</template>

<style scoped>
input {
    width: 50%;
    padding: 5px;
    margin: 5px 0;
}

button {
    padding: 5px;
    margin: 5px 0;
}
</style>