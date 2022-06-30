<template>
  <section>
    <h3>overscroll-behavior</h3>
    <p>○スクロール可能な領域同士が重なっているとき、後の要素のスクロールが連鎖しないようにしてくれる</p>
    <p>○手前の要素に指定</p>
    <p>○overscroll-behavior: contain;</p>
    <div :class="$style.container">
      <div :class="$style.back">
        <p>
          コンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツ
        </p>
      </div>
      <div :class="$style.front">
        <p>
          あああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああああ
        </p>
      </div>
    </div>
    <hr />
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" module>
.container {
  position: relative;
}
.back {
  height: 500px;
  width: 300px;
  overflow-y: scroll;
  background-color: bisque;
  overscroll-behavior: contain;
}
.front {
  position:absolute;
  top:30px;
  left:50px;
  overflow-y: scroll;
  height: 250px;
  width: 150px;
  background-color: pink;
  overscroll-behavior: contain;
}
</style>
