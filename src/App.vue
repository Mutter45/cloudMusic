<template>
  <div class="test">
    test: {{ num }}
    <span>
      ddd
    </span>
  </div>
  <RouterView/>
</template>
<script setup lang="ts">
import { onMounted, ref } from 'vue';
let num = ref(2)
onMounted(() => {
  console.log('onMounted')
})
console.log(num.value)
const addNum = () => {
  num.value++;
}
</script>
<style scoped lang="scss">
.test {
  background-color: antiquewhite;
  > span {
   color: #852727;
  }
}
</style>
