<template>
  <div class="dizme_tm_mobile_menu">
    <div class="mobile_menu_inner">
      <div class="mobile_in">
        <div class="logo">
          <a href="#" style="text-decoration: none;color: black;  font-weight: bold;">
            Kezia Regina
            </a>
        </div>
        <div class="trigger" @click="activeToggle()">
          <div
            class="hamburger hamburger--slider"
            :class="active ? 'is-active' : ''"
          >
            <div class="hamburger-box">
              <div class="hamburger-inner"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="dropdown" :style="{ display: active ? 'block' : 'none' }">
      <div class="dropdown_inner">
        <ul class="anchor_nav">
          <li class="current"><a href="#home">Home</a></li>
          <li><a href="#portfolio">Portfolio</a></li>
          <li><a href="#service">Service</a></li>
          <li><a href="https://medium.com/@keziaregina28">Blog</a></li>
          <li><a href="https://wa.me/6285601487041">WhatsApp</a></li>
          <li><a href="https://www.linkedin.com/in/keziaeci/">LinkedIn</a></li>
          <!-- <li><a href="#contact">Upwork</a></li> -->
          <li><a href="mailto:keziaregina28@gmail.com">Email Me</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileHeader",
  data() {
    return {
      active: false,
    };
  },
  methods: {
    activeToggle() {
      this.active = !this.active;
    },
  },
  props: {
    dark: { type: Boolean },
  },
};
</script>
