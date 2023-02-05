<template>
<Footer/>
<Input/>
</template>

<script>
import Footer from "./components/Footer.vue"
import Input from "./components/Input.vue"

export default {
  name: 'App',
  components: {
  Footer,
  Input
  }
}
</script>

<style>
#app {
  font-family:Helvetica, Arial, sans-serif;
  margin-top: 60px;
  align-items: flex-start;
}
</style>
