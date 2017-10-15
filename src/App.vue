<template>
<section class="hero is-dark is-fullheight">
  <hero-head></hero-head>
  <hero-body></hero-body>
  <hero-foot></hero-foot>
</section>
</template>

<script>
import HeroHead from './components/HeroHead'
import HeroBody from './components/HeroBody'
import HeroFoot from './components/HeroFoot'

export default {
  name: 'app',
  components: {
    HeroHead, HeroBody, HeroFoot
  }
}
</script>

<style>
html {
  overflow-y: auto;
}
</style>
