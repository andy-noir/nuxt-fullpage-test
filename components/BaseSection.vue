<template>
  <section
    :class="`section_${name}`"
    class="section"
  >
    <slot/>
  </section>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>

.section {
  height: 100vh;
  width: 100%;
}
</style>
