<template>
  <div class="right-section">
    <Section
      v-for="section in rightSectionCopy"
      v-bind:sectionHeading="section.sectionHeading"
      v-bind:sectionBody="section.sectionBody"
      v-bind:sectionSubsections="section.subsectionData"
    />
  </div>
</template>

<script>
import Section from './Section.vue'

export default {
  name: 'rightSection',
  props: {
    rightSectionCopy: Object,
  },
  components: {
    Section,
  },
}
</script>
