<template>
  <div class="main-page">
    <header-main/>

    <running-line/>

    <div class="main-content">

      <div class="discription-first">
        <h2> Чтобы поддержать <br>
          Международный васюкинский <br>
          турнир посетите лекцию на тему: <br>
          <span> «Плодотворная дебютная идея» </span>
        </h2>

        <img src="@/assets/discription-first.png" alt="">
      </div>
    </div>
    
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HeaderMain from '@/components/HeaderMain.vue';
import RunningLine from '@/components/RunningLine.vue';

export default defineComponent({
  name: 'HomeView',
  components: {
    HeaderMain,
    RunningLine
  }
});
</script>

<style lang="scss" scoped>

.main-page {

  .main-content {
    padding: 140px 0px;
    max-width: 1222px;
    margin: auto;

    .discription-first {
      display: flex;
      align-items: center;

      h2 {
        margin-right: auto;
        
        line-height: 135%;
        font-family: "Merriweather", serif;
        font-weight: 500;
        font-style: normal;
        font-size: 36px;

        span {
          color: var(--running-line-bg-color);
        }
      }

      img {
        height: 250px;
        width: 394px;
      }
    }
  }
}

</style>
