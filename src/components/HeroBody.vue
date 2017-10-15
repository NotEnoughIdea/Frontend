<template>
<div class="hero-body">
  <div class="container has-text-centered">
    <h1 class="title">{{ message }}</h1>
    <h2 class="subtitle">Pssst... Click on buttons below</h2>
  </div>
</div>
</template>

<script>
import EventManager from '../EventManager'

export default {
  name: 'HeroBody',
  data () {
    return {
      what: '',
      who: '',
      in: ''
    }
  },
  computed: {
    message () {
      return `${this.what} ${this.who} ${this.in}`
    },
    all () {
      return {
        'what': this.request('what'),
        'who': this.request('who'),
        'in': this.request('in')
      }
    }
  },
  created () {
    this.change(['what', 'who', 'in'])
    EventManager.$on('change', this.change)
  },
  methods: {
    change (targets) {
      targets.forEach(target => {
        switch (target) {
          case 'what':
            this.what = this.all.what[Math.floor(Math.random() * this.all.what.length)]
            break
          case 'who':
            this.who = this.all.who[Math.floor(Math.random() * this.all.who.length)]
            break
          case 'in':
            this.in = this.all.in[Math.floor(Math.random() * this.all.in.length)]
            break
        }
      })
    },
    request (page) {
      const request = new XMLHttpRequest()
      request.open('GET', `https://raw.githubusercontent.com/NotEnoughIdea/Ideas/master/resources/${page}.txt`, false)
      request.send()
      return request.responseText.split('\n').map(value => value.trim()).filter(value => !!value)
    }
  }
}
</script>
