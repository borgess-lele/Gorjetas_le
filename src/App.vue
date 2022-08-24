 <script setup>
import { ref } from "vue";

const valor2 = ref("");
const valor1 = ref("");
</script>

<template>
<div>
  <input type="number" v-model="valor1" placeholder="Valor da conta" /> 

  <select name="Qualidade de serviço" id="asd" v-model="gorgeta">
    <option value="5">5% (Péssimo)</option>
    <option value="10">10% (Ruim)</option>
    <option value="15">15% (Ok)</option>
    <option value="20">20% (Bom)</option>
    <option value="25">25% (Mais que bom)</option>
    <option value="25">30% (Exepcional)</option>
  </select>

  <input type="number" placeholder="Quantidade de pessoas" v-model="valor2" />

  <p>Valor da conta : {{ (valor1 * (1 + gorgeta / 100)) / valor2 }}</p>
  </div>
</template>


