<template>
  <h1>App Contador: {{ contador }}</h1>
  <contador-uno />
  <contador-accion />
</template>

<script>
import { provide, ref } from "vue";
import ContadorUno from "@/components/ContadorUno";
import ContadorAccion from "./components/ContadorAccion.vue";
export default {
  name: "App",
  setup() {
    const contador = ref(0);

    provide("contador", contador);

    return {
      contador,
    };
  },
  components: {
    ContadorUno,
    ContadorAccion,
  },
};
</script>
