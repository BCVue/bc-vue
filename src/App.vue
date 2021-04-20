<template>
  <div>
    <BCButton1 Text="Simple Button" radius="20" />
  </div>
</template>

<script>
import BCButton1 from "./assets/components/buttons/simpleBtn";
import BCButton2 from "./assets/components/buttons/simpleBtn2";
export default {
  components: {
    BCButton1,
    BCButton2,
  },
};
</script>

<style lang="scss">
@import "./assets/style/main";
</style>