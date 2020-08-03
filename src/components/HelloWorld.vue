/**
* 感知到的变化：
* 1、每个.vue文件可以不用一个dom元素包裹。
* 2、v-slot父元素中可以用#代替，data数据解构，用法见app.vue.
*/
<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <slot></slot>
  <slot name="center" :data="data"></slot>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0,
      data: ['left', 'center', 'right']
    }
  }
}
</script>
