<template>
  <div class="left-section">
    <Section
      v-for="section in leftSectionCopy"
      v-bind:sectionHeading="section.sectionHeading"
      v-bind:sectionBody="section.sectionBody"
      v-bind:sectionSubsections="section.subsectionData"
    />
  </div>
</template>

<script>
import Section from './Section.vue'

export default {
  name: 'leftSection',
  props: {
    leftSectionCopy: Object,
  },
  components: {
    Section,
  },
}
</script>
