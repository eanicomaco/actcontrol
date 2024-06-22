<script setup lang="ts">
import { ref } from 'vue';
import Temporizador from './Temporizador.vue';

const descricao = ref<string>('');

function finalizarTarefa(tempoDecorrido: number): void {
    emits('aoSalvarTarefa', {
        duracaoEmSegundos: tempoDecorrido,
        descricao: descricao.value,
    });
    descricao.value = '';
}

const emits = defineEmits<{
    (e: 'aoSalvarTarefa', payload: { duracaoEmSegundos: number, descricao: string }): void;
}>()

</script>

<template>
    <div class="box">
        <div class="columns">
            <div class="column is-8" roel="form" aria-label="Formulário para criação de tarefas.">
                <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?" v-model="descricao">
            </div>
            <div class="column">
                <Temporizador @ao-temporizador-finalizado="finalizarTarefa" />
            </div>
        </div>
    </div>
</template>

<style scoped></style>