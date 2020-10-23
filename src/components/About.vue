<template lang="pug">
section#about
  h2 About Me
  .row
    .block.col-12.col-sm-6
      .pic
        .pic-wrap
          img(:src='imgSrc')
        .pattern-diagonal-lines-sm
    .block.col-12.col-sm-6.d-flex.flex-column.justify-content-center.align-items-start
      h5 你好，我是張雅婷
      p Front-End Website Developer
      .intro
        p 大學時接觸到網頁設計的課程，產生濃厚的興趣。
        p 之後參與泰山職訓的專業課程，使網頁設計技能更加精進。
        p 對於 HTML、CSS 及 JavaScript 相當熟悉，
        p 前端使用 Bootstrap、jQuery 與 Vue.js 框架進行網頁開發，
        p 後端運用 Node.js 及 MongoDB 建置資料庫，並配合 Git 執行版本控制‧
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
