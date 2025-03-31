<template>
  <div class="sectionContainer">
    <h2>{{ sectionHeading }}</h2>

    <p v-for="sectionText in sectionBody" v-html="sectionText.text"></p>

    <div v-for="subsection in sectionSubsections" class="subsectionContainer">
      <h3>{{ subsection.subsectionHeading }}</h3>

      <h4>{{ subsection.subsectionSubheading }}</h4>

      <ul v-for="subsectionText in subsection.subsectionBody">
        <li v-html="subsectionText.text"></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'sectionContainer',
  props: {
    sectionHeading: String,
    sectionBody: Array,
    sectionSubsections: Array,
  },
}
</script>
