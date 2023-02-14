<template>
    <div class="box has-text-weight-bold">
      <div class="columns">
        <div class="column is-7">
          {{ tarefa.descricao || "Tarefa sem descrição" }}
        </div>
        <div class="column">
          <FormularioCronometro :tempoEmSegundos="tarefa.duracaoEmSegundos" />
        </div>
      </div>
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from "vue";
import FormularioCronometro from "./FormularioCronometro.vue";
import ITarefa from "../interfaces/ITarefa";

export default defineComponent({
  name: "ListaTarefas",
  components: { FormularioCronometro },
  props: {
    tarefa: {
      type: Object as PropType<ITarefa>,
      required: true,
    },
  },
});
</script>

<style scoped>
.box {
  background: #faf0ca;
}
</style>
