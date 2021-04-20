<template>
  <div class="bc-btn1" ref="bcBtn1">
    {{ Text }}
  </div>
</template>

<script>
export default {
  props: {
    Text: {
      default: "Beauty Component",
      type: String,
    },
  },
  methods: {
    checkAttr() {
      let btn = document.querySelector(".bc-btn1");
    },

    clickRipple() {
      let mainBtn = this.$refs.bcBtn1;
      mainBtn.addEventListener("click", (e) => {
        let rippleSpan = document.createElement("span");
        rippleSpan.classList.add("btn-ripple1");
        mainBtn.appendChild(rippleSpan);
        let pos = mainBtn.getBoundingClientRect();
        rippleSpan.style.left = e.clientX - pos.left - pos.x + "px";
        rippleSpan.style.top = e.clientY - pos.top - pos.y + "px";

        rippleSpan.style.transform = "scale(10)";
        rippleSpan.style.opacity = 0;
        setTimeout(() => {
          mainBtn.removeChild(rippleSpan);
        }, 1000);
      });
    },
  },
  mounted() {
    this.clickRipple();
    this.checkAttr();
  },
};
</script>

<style lang="scss">
@import "../../style/components/buttons/simplebtn";
</style>