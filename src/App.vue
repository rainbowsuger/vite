<template>
  <HelloWorld msg="Hello Vue 3.0 + Vite">
    <template #><h2>this is a slot</h2></template>
    <template v-slot:center="{data}">
      <div class="block-flex">
        <div v-for="item in data" class="mar-right10">{{item}}</div>
      </div>
    </template>
  </HelloWorld>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
