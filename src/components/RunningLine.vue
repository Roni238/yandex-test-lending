<template>
  <marquee>
      <p v-for="(message, index) in messages" :key="index">
        {{ message }}
        <span v-if="index !== messages.length - 1"> • </span>
      </p>
  </marquee>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'running-line',
  props: {
    messages: {
      type: Array,
      required: false,
      default: () => [
        "Дело помощи утопающим — дело рук самих утопающих!",
        "Шахматы двигают вперед не только культуру, но и экономику!",
        "Лед тронулся, господа присяжные заседатели!"
      ]
    }
  },
});
</script>

<style scoped lang="scss">

marquee {
    font-size: 22px;
    padding: 2px;
    height: 60px;
    background: var(--running-line-bg-color);
    display: flex;
    align-items: center;
    color: var(--running-line-color);

    p {
      margin: 0;
      white-space: nowrap;
      display: inline;
    }
}

</style>

