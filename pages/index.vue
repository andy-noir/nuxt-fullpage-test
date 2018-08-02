<template>
  <section class="container">
    <ul id="menu">
      <li
      v-for="(section, index) in sections"
      :key="index"
      :data-menuanchor="section.anchor">
        <a :href="section.url">{{ section.title }}</a>
        <!-- <nuxt-link :to="section.url">
          {{ section.title }}
        </nuxt-link> -->
      </li>
    </ul>
    <full-page :options="options" id="fullpage">
      <div class="section">
          <h3>Section 1</h3>
      </div>
      <div class="section">
          <h3>Section 2</h3>
      </div>
      <div class="section">
          <h3>Section 3</h3>
      </div>
      <div class="section">
          <h3>Section 4</h3>
      </div>
      <div class="section">
          <h3>Section 5</h3>
      </div>
    </full-page>
  </section>
</template>

<script>
import BaseSection from '~/components/BaseSection.vue'

export default {
  components: {
    BaseSection,
  },
  data() {
    return {
      sections: [
        {
          anchor: 'page1',
          title: 'Section 1',
          url: '#page1',
        },
        {
          anchor: 'page2',
          title: 'Section 2',
          url: '#page2',
        },
        {
          anchor: 'page3',
          title: 'Section 3',
          url: '#page3',
        },
        {
          anchor: 'page4',
          title: 'Section 4',
          url: '#page4',
          
        },
        {
          anchor: 'page5',
          title: 'Section 5',
          url: '#page5',
        },
      ],
      options: {
          scrollBar: true,
          menu: '#menu',
          anchors: ['page1', 'page2', 'page3', 'page4', 'page5'],
          sectionsColor: ['#41b883', '#ff5f45', '#0798ec', '#fec401', '#1bcee6', '#ee1a59', '#2c3e4f', '#ba5be9', '#b4b8ab']
      },
    };
  }
}
</script>

<style>
.fp-tableCell {
  display: flex;
  position: relative;
  justify-content: center;
  align-items: center;
  width: 100%;
}

 .section {
   display: flex;
   height: 100vh;
   width: 100%;
   justify-content: center;
   align-items: center;
 }

 ul {
   display: flex;
   position: fixed;
   list-style: none;
   margin-top: 20px;
   z-index: 1;
 }

 ul li {
   margin: 0 15px;
 }

 ul li a {
   text-decoration: none;
   color: #fff;
 }
  ul li a:hover {
   color: red;
 }
</style>
