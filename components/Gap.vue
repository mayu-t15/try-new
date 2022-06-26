<template>
  <section>
    <h3>gap</h3>
    <p>○ CSS Gridのみで使えていた→flex, grid, multi-column</p>
    <p>○ gap: row-gap column-gap(gap: 50px 20px)</p>
    <p>○ ブラウザ対応: 最新モダンブラウザOK</p>
    <div :class="$style.gap_container">
      <div :class="$style.gap_child"></div>
      <div :class="$style.gap_child"></div>
      <div :class="$style.gap_child"></div>
      <div :class="$style.gap_child"></div>
      <div :class="$style.gap_child"></div>
      <div :class="$style.gap_child"></div>
    </div>
    <hr />
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" module>
// Before(調整してない)
// .gap {
//   &_container {
//     display: flex;
//     justify-content: center;
//     flex-wrap: wrap;
//     padding: 20px;
//     align-items: center;
//     width: 500px;
//     background-color: #000;
//   }
//   &_child {
//     background-color: white;
//     width: 100px;
//     height: 100px;
//     margin-top: 50px;
//     margin-left: 50px;
//     &:first-of-type {
//       margin-left: 0;
//     }
//   }
// }
// After -gap使用
.gap {
  &_container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 500px;
    padding: 50px;
    align-items: center;
    gap: 50px 50px; // ←これだけ
    background-color: #000;
  }
  &_child {
    background-color: white;
    width: 100px;
    height: 100px;
  }
}
</style>
