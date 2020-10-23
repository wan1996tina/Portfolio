<template lang="pug">
#main-content
  nav#navbar(ref="navbar")
    ul
      li
        a(href="javascript:void(0)" @click="scrollTo('#hero')") Home
        .fai
          font-awesome-icon(:icon="['fas','home']" href="javascript:void(0)" @click="scrollTo('#hero')")
      li
        a(href="javascript:void(0)" @click="scrollTo('#about')") About Me
        .fai
          font-awesome-icon(:icon="['fas','user']" href="javascript:void(0)" @click="scrollTo('#about')")
      li
        a(href="javascript:void(0)" @click="scrollTo('#skill')") Skill
        .fai
          font-awesome-icon(:icon="['fas','tools']" href="javascript:void(0)" @click="scrollTo('#skill')")
      li
        a(href="javascript:void(0)" @click="scrollTo('#resume')") Resume
        .fai
          font-awesome-icon(:icon="['fas','address-card']" href="javascript:void(0)" @click="scrollTo('#resume')")
      li
        a(href="javascript:void(0)" @click="scrollTo('#portfolio')") Portfolio
        .fai
          font-awesome-icon(:icon="['fas','palette']" href="javascript:void(0)" @click="scrollTo('#portfolio')")
  <hero></hero>
  <about></about>
  <skill></skill>
  <resume></resume>
  <portfolio></portfolio>
  <myfooter></myfooter>
</template>

<script>
import hero from '@/components/Hero.vue'
import navbar from '@/components/Navbar.vue'
import about from '@/components/About.vue'
import skill from '@/components/Skill.vue'
import resume from '@/components/Resume.vue'
import portfolio from '@/components/Portfolio.vue'
import myfooter from '@/components/Footer.vue'

export default {
  components: {
    hero,
    navbar,
    about,
    skill,
    resume,
    portfolio,
    myfooter
  },
  methods: {
    scrollTo (selector) {
      const scroll = this.$el.querySelector(selector)
      // document.documentElement.scrollTop = scroll.offsetTop
      // document.body.scrollTop = scroll.offsetTop
      // window.pageYOffset = scroll.offsetTop

      window.scrollTo({
        top: scroll.offsetTop,
        behavior: 'smooth'
      })
    }
  },
  mounted () {
    const nav = this.$refs.navbar
    window.onscroll = () => {
      // console.log(document.body.clientWidth)
      console.log(document.documentElement.scrollTop)
      if (window.scrollY > 100) {
        if (document.body.clientWidth > 992) {
          nav.style.background = 'rgb(232, 224, 255)'
        }
      } else {
        nav.style.background = '#ffffff'
      }
    }
  }
}
</script>
