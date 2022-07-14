<template>
  <div :class="{ clinte: !isPreminm, cliente_prime: isPreminm }">
    <h4>Nome: {{ clientes.nome }}</h4>
    <hr />
    <hr />
    <p>Numero: {{ clientes.numero }}</p>
    <p>Email: {{ clientes.email }}</p>
    <p v-if="verIdade">Idade: {{ clientes.idade }}</p>
    <p v-else>Idade: nao tenho</p>
    <button @click="mudarcor">mudar de cor</button>
  </div>
</template> 
<script>
export default {
  data() {
    return { isPreminm: false };
  },
  props: {
    clientes: Object,
    verIdade: Boolean,
  },
  methods: {
    mudarcor: function () {
      this.isPreminm = !this.isPreminm;
    },
  },
};
</script>

<style scoped>
.cliente {
  background-color: #f5f5fd;
  padding: 1rem;
  height: 200px;
  max-width: 350px;
  margin-top: 1rem;
}
.cliente_prime {
  background-color: #0000ff;
  padding: 1rem;
  height: 200px;
  max-width: 350px;
  margin-top: 1rem;
}
</style>