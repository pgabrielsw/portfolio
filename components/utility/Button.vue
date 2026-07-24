<template>
  <nuxt-link class="inline-block" :to="linkTo">
    <svg
      ref="btnSvg"
      xmlns="http://www.w3.org/2000/svg"
      width="220"
      height="60"
      viewBox="0 0 220 60"
    >
      <rect
        x="0"
        y="0"
        width="60"
        height="60"
        rx="30"
        ry="30"
        fill="#3b82f6"
        style="opacity: 0.4;"
      />
      <text
        transform="translate(80 38)"
        text-anchor="middle"
        font-size="20"
        fill="#000"
      >
        {{ displayTitle }}
      </text>
    </svg>
  </nuxt-link>
</template>

<script>
import { gsap, Elastic, Linear } from 'gsap';

export default {
  mounted() {
    this.$nextTick(() => {
      this.animateButtonOnHover();
    });
  },
  props: {
    displayTitle: String,
    linkTo: String
  },
  methods: {
    animateButtonOnHover() {
      const btn = this.$refs.btnSvg;
      if (!btn) return;

      btn.addEventListener('mouseenter', animate);
      btn.addEventListener('mouseleave', animate);

      const tl = gsap.timeline({ paused: true });
      tl.to(btn.children[0], 0.4, {
        attr: { width: 160, fill: '#3b82f6' },
        autoAlpha: 0.8,
        ease: Elastic.easeOut.config(1, 1)
      });
      tl.to(btn.querySelector('text'), 0.2, { fill: '#f2f0ee', ease: Linear.easeNone }, 0);
      tl.reverse();

      function animate() {
        tl.reversed(!tl.reversed());
      }
    }
  }
};
</script>

<style lang="scss" scoped>
svg {
  font-weight: 700;
  overflow: visible;
}
</style>
