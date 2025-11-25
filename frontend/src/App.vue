<script lang="ts" setup>
import { initGeetest4 } from './assets/gt4.js'

const testBtn = async () => {
  try {
    const i = await initGeetest4({
      captchaId: "dd79f9ac1a3c66fc21e6df7cecab4d40",
      product: "bind",
      riskType: "slide",
    })
    console.log(i);
  } catch (e) {
    console.error(e)
  }
}
</script>

<template>
  <div style="height: 100vh; display: flex; justify-content: center; align-items: center;">
    <button @click="testBtn">test</button>
  </div>
</template>

<style></style>
