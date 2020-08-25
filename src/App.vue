<template>
  <div id="app">
      <Header title="Bonjour" desc="Tout le monde" />
      <Computed />
      <Section />
  </div>
</template>

<script>
import Header from './components/header'
import Computed from "./components/computed"
import Section from "./components/section"

export default {
  name: 'App',
  components: {
    Header,
    Computed,
    Section

    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
