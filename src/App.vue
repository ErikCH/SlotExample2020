<template>
  <div id="app">Hello World</div>
  <Child v-slot="{data, hello}">
    <button @click="pressed()">Press Me</button>
    {{data}}
    <br />
    <button @click="hello">Child Component Button</button>
  </Child>
</template>

<script>
import Child from '@/components/Child.vue';

export default {
  name: 'App',
  components: {
    Child
  },
  methods: {
    pressed(){
      alert('hello from parent')
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
