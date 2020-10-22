<template lang="pug">
section#about
  h2 About Me
  .row
    .block.col-12.col-sm-6
      .pic
        .pic-wrap
          img(:src='imgSrc' width="300px")
        .pattern-diagonal-lines-sm
    .block.col-12.col-sm-6.d-flex.flex-column.justify-content-center.align-items-start
      h5 你好，我是張雅婷
      p Front-End Website Developer
      .intro
        p 大學時，接觸到寫網頁後產生興趣。
        p 畢業後參與泰山職訓的專業課程，使專業技能更加精進。
        p 經過 936 小時的課程，紮實學習 HTML、CSS 及 JavaScript
        p 前端能使用 Bootstrap、jQuery 套件與 Vue.js 框架
        p 後端可利用 Node.js 進行資料存取，並配合 Git 控管專案版本
//- pattern-dots-md
</template>

<script>
export default {
  data () {
    return {
      imgSrc: './12893070347656.jpg'
    }
  }
}
</script>
