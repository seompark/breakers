<template>
  <div class="shop">
    <div class="hero">
      <v-navbar white/>
    </div>
    <div class="goods">
      <section class="goods__section">
        <h3 class="goods__section-title">인기순 최근등록순 판매량순 가격낮은순 가격높은순</h3>
        <hr class="divider">
        <div class="goods__cards">
          <div
            v-for="(card, i) in cards"
            :key="`goods-${i}`"
            class="goods__card">
            <img
              class="goods__card-img"
              :src="card.src">
            <div class="goods__card-info">
              <p class="goods__card-title">{{card.title}}</p>
              <p class="goods__card-author">{{card.author}}</p>
              <p class="goods__card-price">{{card.price}}</p>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import VNavbar from '@/components/VNavbar.vue'

export default {
  name: 'Funding',
  components: { VNavbar },
  data () {
    return {
      cards: [
        {
          title: '휴집; 그들이 담긴 시집',
          author: '공동작품',
          price: '25,000 원',
          src: require('@/assets/images/goods/shop-1.png')
        },
        {
          title: '쉬어가는 머그컵',
          author: '노경숙',
          price: '10,000 원',
          src: require('@/assets/images/goods/shop-2.png')
        },
        {
          title: '쉬어가는 티셔츠',
          author: '노경숙',
          price: '24,900 원',
          src: require('@/assets/images/goods/shop-3.png')
        },
        {
          title: '쉬어가는 플립화',
          author: '노경숙',
          price: '35,000 원',
          src: require('@/assets/images/goods/shop-4.png')
        },
        {
          title: 'I WANT CHANGE',
          author: '신해철',
          price: '19,900 원',
          src: require('@/assets/images/goods/shop-5.png')
        },
        {
          title: '손에 손잡고',
          author: '서문탁',
          price: '4,900 원',
          src: require('@/assets/images/goods/shop-6.png')
        },
        {
          title: '봄 날은 온다',
          author: '구영훈',
          price: '4,900 원',
          src: require('@/assets/images/goods/shop-7.png')
        },
        {
          title: '쉬어가는 에코백',
          author: '박수경',
          price: '24,000 원',
          src: require('@/assets/images/goods/shop-8.png')
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.shop {
  background-color: #f9f9f9;
}

.hero {
  background: url("../assets/images/shop-hero-1.png") center top no-repeat;
  background-size: 100% auto;
  height: 500px;
}

.divider {
  border: 0;
  border-bottom: 2px solid #d2d2d2;
}

.goods {

}

.goods__section {
  margin: 70px;
}

.goods__section-title {
  font-family: 'Nanum Square', sans-serif;
  font-size: 14px;
  word-spacing: 20px;
}

.goods__cards {
  display: flex;
  flex-wrap: wrap;
  margin: 0; padding: 0;
}

.goods__card {
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
  width: 25%;
  padding: 20px;
  height: 100%;
}

.goods__card-img {
  cursor: pointer;
}

.goods__card-info {
  font-family: 'Nanum Square', sans-serif;
  width: 100%;
  text-align: center;
  cursor: pointer;
}

.goods__card-title {
  display: block;
  margin: 1rem 0 0 0;
  font-weight: bold;
}

.goods__card-author {
  display: block;
  margin: 0.35rem 0 0 0;
  font-weight: bold;
  color: #a5a5a5;
}

.goods__card-price {
  display: block;
  margin: 0.35rem 0 0 0;
}

.goods__section-title-gray {
  color: #cccccc;
}
</style>
