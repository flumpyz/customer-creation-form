<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <CustomerForm />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import CustomerForm from "@/components/CustomerForm";

export default {
  name: 'App',
  components: {
    // eslint-disable-next-line vue/no-unused-components
    HelloWorld,
    CustomerForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
