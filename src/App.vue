<template>
  <div id="app">
    <div v-for="(clientes,inidex) in clientes" :key="clientes.id">
     {{inidex}}
      <Cliente :clientes="clientes" :verIdade="true" />
    </div>
  </div>
</template>

<script>
import Cliente from "./components/Cliente";
export default {
  name: "App",
  data() {
    return {
      clientes: [
        {
          id:1,
          nome: "isso",
          email: "tesste@",
          numero: "456",
          idade: "1",
        },
        {
          id:2,
          nome: "isso",
          email: "tesste@",
          numero: "456",
          idade: "1",
        },
        {
          id:3,
          nome: "isso",
          email: "tesste@",
          numero: "456",
          idade: "1",
        },
      ],
    };
  },
  components: {
    Cliente,
  },
};
</script>

<style>
</style>
