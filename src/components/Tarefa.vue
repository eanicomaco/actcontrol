<script setup lang="ts">
import { ref } from 'vue';
import Cronometro from './Cronometro.vue';
import type ITarefa from '@/interfaces/ITarefa';
import Box from './Box.vue';

const props = defineProps<{
    tarefa: ITarefa;
}>()

</script>

<template>
    <Box>
        <div class="columns">
            <div class="column is-7">
                {{ tarefa.descricao || 'Tarefa padrão' }}
            </div>
            <div class="column">
                <Cronometro :tempo-em-segundo="tarefa.duracaoEmSegundos" />
            </div>
        </div>
    </Box>
</template>

<style scoped></style>