<template>
  <header>
    <h1>NICOLE GATMAITAN</h1>
    <h2>Front-End Developer</h2>
  </header>

  <main>
    <LeftSection v-bind:leftSectionCopy="myJson[0]" />
    <RightSection v-bind:rightSectionCopy="myJson[1]" />
  </main>

  <footer>
    <div id="copyright">© {{ new Date().getFullYear() }} Nicole Gatmaitan</div>
  </footer>
</template>

<script>
import LeftSection from './components/LeftSection.vue'
import RightSection from './components/RightSection.vue'
import json from './assets/data.json'

export default {
  name: 'Body',
  data() {
    return {
      myJson: json,
    }
  },
  components: {
    LeftSection,
    RightSection,
  },
}
</script>

<style scoped>
header {
  text-align: center;
  background: url('./assets/circle.png');
  background-size: 360px;
  background-repeat: no-repeat;
  background-position: center;
  padding: 50px 0;
}

header h1 {
  font-size: 3em;
  line-height: 1.25;
  font-weight: normal;
}

footer {
  margin-bottom: 10px;
  text-align: center;
}

@media (min-width: 768px) {
  header {
    padding: 100px 0;
  }
  header h1 {
    font-size: 3.5em;
    line-height: 1.5;
  }
}
</style>
