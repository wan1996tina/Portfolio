<template lang="pug">
#main-content
  nav#navbar(ref="navbar")
    ul
      li
        a(href="javascript:void(0)" @click="scrollTo('#hero')") Home
      li
        a(href="javascript:void(0)" @click="scrollTo('#about')") About Me
      li
        a(href="javascript:void(0)" @click="scrollTo('#skill')") Skill
      li
        a(href="javascript:void(0)" @click="scrollTo('#resume')") Resume
      li
        a(href="javascript:void(0)" @click="scrollTo('#portfolio')") Portfolio
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
        if (document.body.clientWidth > 992) { nav.style.background = 'rgb(232, 224, 255)' }
      } else {
        nav.style.background = 'rgba(232, 224, 255, .8)'
      }
    }
  }
}
</script>
