<template>
  <ClientOnly>
  <div class="tp-marquee-area z-index-5">
    <div class="tp-marquee-wrapper">
      <div class="tp-marquee-slider fix">
        <div class="tp-marquee-slider-active d-flex align-items-center">
          <Vue3Marquee :duration="30" :animateOnOverflow="true">
            <div
              v-for="(m, i) in marquee_data"
              :key="i"
              class="tp-marquee-item"
            >
              <p>{{ m.text }} <img :src="m.img" alt="" /></p>
          </div>
          </Vue3Marquee>
        </div>
      </div>
    </div>
  </div>
  </ClientOnly>
</template>

<script setup lang="ts">
const marquee_data = [
  { text: "Graphic Designer", img: "/images/marquee/smile.svg" },
  { text: "Visual Storytelling", img: "/images/marquee/stroke.svg" },
  { text: "Branding", img: "/images/marquee/smile.svg" },
  { text: "Logo Design", img: "/images/marquee/stroke.svg" },
  { text: "Motion Graphics", img: "/images/marquee/smile.svg" },
  { text: "Creative Design Solutions", img: "/images/marquee/stroke.svg" },
  { text: "Social Media Creatives", img: "/images/marquee/stroke.svg" },
  { text: "Video Editing", img: "/images/marquee/stroke.svg" },
];
</script>
