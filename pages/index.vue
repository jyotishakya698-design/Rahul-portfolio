<template>
  <div>
    <nuxt-layout name="layout-one">
      
    <!-- hero banner -->
    <hero-banner-one id="home" />
    <!-- hero banner -->


    <!-- service area -->
    <service-area-one />
    <!-- service area -->

    <!-- marquee area -->
    <marquee-area />
    <!-- marquee area -->

    <!-- about area -->
    <about-area-one id="about-me" />
    <!-- about area -->

    <!-- portfolio area -->
    <project-one id="portfolio" />
    <!-- portfolio area -->

    <!-- skill area -->
    <skill-area id="skills" />
    <!-- skill area -->

    

    </nuxt-layout>
  </div>
</template>

<script setup lang="ts">
useSeoMeta({ title: "Rahul Rahul R - Graphic Designer, Video Editor" });
definePageMeta({ layout: false });
import {animatedHeadline} from '@/utils/animatedHeadline';
import {buttonAnimation} from '@/utils/buttonAnimation';

onMounted(() => {
  useSmoothScroll();
  
  setTimeout(() => {
    animatedHeadline();
    useAnimationTitle();
    buttonAnimation();
    useScrollTextAnimation();
  },0)
})
</script>
