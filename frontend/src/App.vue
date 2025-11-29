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

const testBtn2 = (url: string) => {
  var head = document.getElementsByTagName("head")[0];
  var script = document.createElement("script");
  script.charset = "UTF-8";
  script.async = true;
  script.onerror = function () {
    alert("load error");
  };
  script.onload = function () {
    alert("load done");
  };
  script.src = url;
  head.appendChild(script);
};
</script>

<template>
  <div style="height: 100vh; display: flex; justify-content: center; align-items: center;">
    <button @click="testBtn2('https://pss.bdstatic.com/static/superman/js/components/tips-e2ceadd14d.js')">test</button>
  </div>
</template>

<style></style>
