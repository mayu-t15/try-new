<template>
  <section>
    <h3>Scroll snap</h3>
    <p>○ 少しのスクロールでピタッと止まって欲しい</p>
    <p>
      ○ 親）scroll-snap-type:<br />
      ・スクロールスナップコンテンツか<br />
      ・どの軸を考慮するか(x, y, both )<br />
      ・どの程度厳密にスナップするか(default=proximity or mandatory)<br />
    </p>
    <p>子）</p>
    <p>○ ブラウザ対応: 最新モダンブラウザOK</p>
    <div :class="$style.snap_container">
      <div :class="$style.snap_child" style="background-color: #f7e1a6">
        <p>slide 1</p>
      </div>
      <div :class="$style.snap_child" style="background-color: #f7b5a6">
        <p>slide 2</p>
      </div>
      <div :class="$style.snap_child" style="background-color: #bfedff">
        <p>slide 3</p>
      </div>
      <div :class="$style.snap_child" style="background-color: #f7e1a6">
        <p>slide 3</p>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" module>
.snap {
  &_container {
    display: flex;
    overflow-x: scroll;
    // 以下を追加
    scroll-snap-type: x mandatory;
    width: 1000px;
    padding: 30px;
  }
  &_child {
    flex: 0 0 auto;
    white-space: nowrap;
    // 以下を追加
    scroll-snap-align: start;
    width: 700px;
    height: 200px;
    text-align: center;
    & > p {
      padding-top: 70px;
    }
  }
}
</style>
