<template>
  <section id="tp-sv" class="tp-services-area tp-sv tp-services-bg-text-animation fix">
      <div class="container container-large">
        <div class="tp-services-inner pb-195 p-relative z-index-1">

            <span class="tp-services-inner-border tp-vertical-line transition-3"></span>
            <span class="tp-services-inner-border right tp-vertical-line transition-3"></span>

            <div class="tp-services-bottom-text tp-services-bg-text ">
              <p>Services</p>
            </div>
            <div class="row gx-0">
              <div class="col-xl-6 col-lg-7">
                  <div class="tp-services-wrapper tp-services-capsule-wrapper p-relative  pt-100 pr-70"
                    data-tp-throwable-scene="true">
                    <div class="tp-section-title-wrapper tp_text_anim mb-170">
                        <div class="tp-section-title-inner p-relative">
                          <span class="tp-section-subtitle">Services</span>
                          <h3 class="tp-section-title tp_title_anim">Solution <br> we provide.</h3>
                        </div>
                        <p>The combination of my passion for design, code & interaction web design world.</p>
                    </div>
                    <!-- service capsule items -->
                    <service-capsule-items />
                    <!-- service capsule items -->
                  </div>
              </div>
              <div class="col-xl-6 col-lg-5">
                  <div class="tp-services-accordion tp-accordion tp-accordion-2 mt-90 pl-70 p-relative">
                    <span class="tp-services-accordion-border"></span>
                    <div class="accordion" id="accordionExample">
                        <div v-for="(item) in accordion_data" :key="item.id" :class="`accordion-item tp-services-accordion-item ${item.active ? 'active' :''}`">
                          <h2 class="accordion-header" :id="`heading-${item.tab_id}`">
                              <button :class="`accordion-button ${item.active ? '' : 'collapsed'}`" type="button"
                                data-bs-toggle="collapse" :data-bs-target="`#collapse-${item.tab_id}`" :aria-expanded="`${item.active ? 'true' : 'false'}`" :aria-controls="`collapse-${item.tab_id}`">
                                <span>{{`${item.id > 11 ? item.id : `0${item.id}`}`}}</span>
                                {{item.question}}
                              </button>
                          </h2>
                          <div :id="`collapse-${item.tab_id}`" :class="`accordion-collapse collapse ${item.active ? 'show' : ''}`" :aria-labelledby="`heading-${item.tab_id}`" data-bs-parent="#accordionExample">
                              <div class="accordion-body">
                                <p>{{item.answer}} </p>
                                <ul>
                                    <li v-for="(l,i) in item.lists" :key="i">{{l}}</li>
                                </ul>
                              </div>
                          </div>
                          <span class="accordion-item-border"></span>
                        </div>
                    </div>
                  </div>
              </div>
            </div>
        </div>
      </div>
  </section>
</template>

<script setup lang="ts">
import throwableAnimation from '@/utils/throwableAnim';

const accordion_data = [
    {
      id: 1,
      tab_id: "one",
      question: "Logo Design",
      lists: [
        "Unique and memorable brand identity concepts",
        "Modern, minimal, and professional logo styles",
        "High-resolution files for web, print, and branding use",
      ]
    },
    {
      id: 2,
      tab_id: "two",
      active:true,
      question: "Brochure Design",
      lists: [
        "Clean and professional multi-page layouts",
        "Creative visuals that highlight services or products",
        "Print-ready and digital brochure formats",
      ]
    },
    {
      id: 3,
      tab_id: "three",
      question: "Flyer / Mailer Design",
      lists: [
        "Eye-catching promotional flyer designs",
        "CStrong typography and visual hierarchy",
        "Designed for both digital sharing and print",
      ]
    },
    {
      id: 4,
      tab_id: "four",
      question: "Letterhead Design",
      lists: [
        "Professional corporate stationery design",
        "Brand-aligned typography and layout",
        "Print-ready formats for official documents",
      ]
    },
    {
      id: 5,
      tab_id: "five",
      question: "Corporate PPT Design",
      lists: [
        "Modern and engaging presentation slides",
        "Clean layouts with professional infographics",
        "Designed to impress clients and stakeholders",
      ]
    },
    {
      id: 6,
      tab_id: "Six",
      question: "Social Media Posts Design",
      lists: [
        "Creative and scroll-stopping social media graphics",
        "Consistent brand style across all posts",
        "Optimized designs for Instagram, Facebook, and LinkedIn",
      ]
    },
    {
      id: 7,
      tab_id: "Seven",
      question: "Catalogue Design",
      lists: [
        "Organized and visually appealing product layouts",
        "Clear product information with strong visuals",
        "Print-ready and digital catalogue versions",
      ]
    }, 
    {
      id: 8,
      tab_id: "Eight",
      question: "Branding Collateral",
      lists: [
        "Business cards, stationery, and marketing materials",
        "Consistent brand identity across all assets",
        "Professional designs for strong brand presence",
      ]
    },
    {
      id: 9,
      tab_id: "Nine",
      question: "UI/UX Design (Web & Mobile)",
      lists: [
        "User-friendly website and mobile app interfaces",
        "Modern UI with smooth user experience",
        "Wireframes, prototypes, and high-quality design layouts",
      ]
    },
    {
      id: 10,
      tab_id: "Ten",
      question: "Video Editing",
      lists: [
        "Professional editing for ads, reels, and promos",
        "Smooth transitions, effects, and motion graphics",
        "Optimized videos for social media and marketing",
      ]
    },
  ];


  onMounted(() => {
    throwableAnimation();
  })
</script>