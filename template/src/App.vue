<template>
  <div id="app">
    <img src="./assets/logo.png">
    {{#router}}
    <router-view/>
    {{else}}
    <Component1/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import Component1 from './components/Component1'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    Component1
  }{{/router}}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
