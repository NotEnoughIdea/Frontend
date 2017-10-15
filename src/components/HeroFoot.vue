<template>
<div class="hero-foot">
  <nav class="tabs is-boxed is-fullwidth">
    <div class="container">
      <ul>
        <li class="is-active" @click="change('what,who,in')"><a>Randomize !</a></li>
        <li><a @click="change('what')">What ?</a></li>
        <li><a @click="change('who')">For who ?</a></li>
        <li><a @click="change('in')">In ?</a></li>
      </ul>
    </div>
  </nav>
</div>
</template>

<script>
import EventManager from '../EventManager'

export default {
  name: 'HeroFoot',
  methods: {
    change (targets) {
      EventManager.$emit('change', targets.split(','))
    }
  }
}
</script>
