<template>
  <div>
    <vuedemoNpmPractice :propData="initData" />
  </div>
</template>

<script>
import vuedemoNpmPractice from "./components/Main.vue";
export default {
  data() {
    return {
      initData: "hello 你好"
    };
  },
  components: {
    vuedemoNpmPractice
  }
};
</script>

<style></style>
