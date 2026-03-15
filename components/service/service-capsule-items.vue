<template>
  <div class="tp-services-capsule-item-wrapper">
    <p v-for="(s, i) in services" :key="i" data-tp-throwable-el="">
      <span
        class="tp-services-capsule-item"
        :data-bg-color="s.bgColor"
        :data-text-color="`${s.textColor ? s.textColor : ''}`"
        :style="{ backgroundColor: s.bgColor, color: s.textColor }"
      >
        {{ s.name }}
      </span>
    </p>
    <p data-tp-throwable-el="">
      <span>
        <img src="/images/services/shape/services-shape-1.png" alt="" />
      </span>
    </p>
    <p data-tp-throwable-el="">
      <span>
        <img src="/images/services/shape/services-shape-2.png" alt="" />
      </span>
    </p>
  </div>
</template>

<script setup lang="ts">
const services = [
  { name: "Brochure Design", bgColor: "#00CC97" },
  { name: "Logo Design", bgColor: "#FF759C" },
  { name: "Flyer / Mailer Design", bgColor: "#FFDB59", textColor: "#121212" },
  { name: "Letterhead Design", bgColor: "#FFDB59", textColor: "#121212" },
  { name: "Corporate PPT Design", bgColor: "#00CC97" },
  { name: "UI/UX Design (Web & Mobile)", bgColor: "#19B3F1" },
  { name: "Social Media Posts Design", bgColor: "#FF759C" },
  { name: "Catalogue Design", bgColor: "#FFDB59", textColor: "#121212" },
  { name: "Branding Collateral", bgColor: "#FF759C" },
  { name: "Video Editing", bgColor: "#00CC97" },
];
</script>
