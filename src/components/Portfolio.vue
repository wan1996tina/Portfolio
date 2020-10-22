<template lang="pug">
section#portfolio
  h2 Portfolio

  .row
    .card(v-for='(item, index) in items')
      .img
        img(:src='item.imgSrc' width="320px")
      .text
        h5 {{ item.title }}
        p {{ item.info }}
        .btn1(@click="demo(item.url)") View
    .d-none.d-xl-block.box
    .card(v-for='(item, index) in items2')
      .img
        img(:src='item.imgSrc' width="340px")
      .text
        h5 {{ item.title }}
        p {{ item.info }}
        .btn1(@click="demo(item.url)") View
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          imgSrc: ['/番茄鐘.png'],
          title: '番茄鐘',
          info: '進行時間倒數、新增/修改待辦事項、選擇響鈴。',
          url: 'https://wan1996tina.github.io/pomodoro/'
        },
        {
          imgSrc: ['/zen-garden.png'],
          title: 'CSS Zen Garden',
          info: '在html結構不更動的情況下，練習css手刻切版。',
          url: 'https://wan1996tina.github.io/zen-garden/'
        },
        {
          imgSrc: ['/mole.png'],
          title: '打地鼠遊戲(口罩版)',
          info: '以JavaScript練習撰寫打地鼠遊戲，圖片使用免費素材加以修改。',
          url: 'https://wan1996tina.github.io/whac-a-mole/'
        }
      ],
      items2: [
        {
          imgSrc: ['/recipe.png'],
          title: 'Line機器人-食食有譜',
          info: '可以關鍵字搜尋食譜的機器人，使用cheerio進行網頁爬蟲',
          url: 'https://github.com/wan1996tina/nodejs_linebot'
        },
        {
          imgSrc: ['/workout.png'],
          title: 'Workout',
          info: '一個附計時器的居家鍛鍊動作教學網站，計時器專為此類鍛鍊而設計，可設定秒數、循環等，使用者註冊後可儲存計時器。',
          url: 'https://wan1996tina.github.io/project/'
        },
        {
          imgSrc: ['/slapjack.png'],
          title: '簡易版心臟病小遊戲',
          info: '使用jQuery撰寫的小遊戲，玩法與心臟病相同，由電腦出牌，玩家只需點擊對的卡片。',
          url: 'https://wan1996tina.github.io/Slapjack/'
        }
      ]
    }
  },
  methods: {
    demo (url) {
      window.open(url)
    }
  }
}
</script>
