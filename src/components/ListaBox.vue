<template>
    <div class="box has-text-weight-bold">
        Você não possui tarefas registradas!!
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ListaBox'
})
</script>

<style scoped>
.box {
    background: #FAF0CA;
    padding: 1.25rem;
}
</style>