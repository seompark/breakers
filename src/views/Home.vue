<template>
  <div class="home">
    <section class="main">
      <v-navbar/>
      <div class="main__cp-wrapper">
        <p class="main__cp">
          느린 게 아니라, <br>
          뒤쳐진 게 아니라,
        </p>
        <p class="main__cp">
          잠시 <span class="main__cp-emphasize">쉬어가는</span> 중.
        </p>
      </div>
      <div class="main__illust">
        <img
            src="@/assets/images/main-illust.png"
            class="main__illust-img">
      </div>
    </section>
  </div>
</template>

<script>
import VNavbar from '@/components/VNavbar.vue'

export default {
  name: 'Home',
  components: {
    VNavbar
  }
}
</script>

<style lang="scss" scoped>

.main {
  height: 100vh;
}

.main__cp-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: calc(100vh - 280px);
  margin-left: 100px;
  overflow: auto;
}

.main__cp {
  font-family: "Nanum Square", sans-serif;
  font-size: 64px;
  font-weight: lighter;
  margin: 30px 0;
}

.main__cp-emphasize {
  position: relative;
  &:after {
    content: "";
    position: absolute;
    background: rgb(197, 194, 255);
    height: 50px;
    width: 100%;
    bottom: -5px; left: 0;
    z-index: -1;
  }
}

.main__illust-img {
  position: absolute;
  top: 150px; right: 0;
  height: 600px;
  z-index: -1;
}

</style>
