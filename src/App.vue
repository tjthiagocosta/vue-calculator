<template>
    <div id="app">
        <h1>Calculadora Aritmética</h1>
        <h3>Insira dois números e selecione a operação desejada para obter o resultado.</h3>
        <ArithmeticCalculator />
    </div>
</template>

<script>
import ArithmeticCalculator from './components/ArithmeticCalculator.vue';

export default {
    name: 'App',
    components: {
        ArithmeticCalculator
    }
};
</script>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #f5f7fa;
}

h1 {
  font-size: 2.5em;
  color: #34495e;
  margin-bottom: 0.5em;
  letter-spacing: 1px;
}

h3 {
  font-size: 1.2em;
  color: #7f8c8d;
  margin-bottom: 1.5em;
  max-width: 80%;
  margin-left: auto;
  margin-right: auto;
  line-height: 1.4;
}

</style>