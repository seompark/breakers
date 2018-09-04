<template>
  <div class="funding">
    <div class="hero">
      <v-navbar white/>
    </div>
    <div class="nanum">
      <section class="nanum__section">
        <h3 class="nanum__section-title">지금 뜨고 있는 나눔 <span class="nanum__section-title-gray">&gt;</span></h3>
        <div class="nanum__cards">
          <img
            v-for="(card, i) in cards"
            :key="`nanum-${i}`"
            class="nanum__card"
            :src="card">
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
        require('@/assets/images/nanums/card-1.png'),
        require('@/assets/images/nanums/card-2.png'),
        require('@/assets/images/nanums/card-3.png'),
        require('@/assets/images/nanums/card-4.png'),
        require('@/assets/images/nanums/card-5.png'),
        require('@/assets/images/nanums/card-6.png'),
        require('@/assets/images/nanums/card-7.png'),
        require('@/assets/images/nanums/card-8.png')
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.funding {
  background-color: #f9f9f9;
}

.hero {
  background: url("../assets/images/funding-hero-1.png") center top no-repeat;
  background-size: 100% auto;
  height: 500px;
}

.nanum {

}

.nanum__section {
  margin: 70px;
}

.nanum__section-title {
  font-family: 'Nanum Square', sans-serif;
  font-size: 14px;
}

.nanum__cards {
  display: flex;
  flex-wrap: wrap;
}

.nanum__card {
  cursor: pointer;
  width: 25%;
  height: 100%;
}

.nanum__section-title-gray {
  color: #cccccc;
}
</style>
