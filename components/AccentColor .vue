<template>
  <section>
    <h3>accent-color</h3>
    <p>○ input系→スタイルをつけるのが面倒</p>
    <p>○ checkbox, radio, range, progressで使える</p>
    <p>○ チェックの色は指定していないが、ブラウザがよしなにしてくれる</p>
    <p>○ ブラウザ対応: 最新モダンブラウザOKーsafari対応!</p>
    <div :class="$style.container">
      <label>
        Checkbox
        <input type="checkbox" checked />
        <input type="checkbox" checked style="accent-color: #74992e" />
        <input type="checkbox" checked style="accent-color: hsl(250, 100%, 34%);" />
      </label>

      <label>
        Radio Buttons
        <fieldset>
          <input type="radio" name="accented-demo" checked />
          <input type="radio" name="accented-demo" />
          <input type="radio" name="accented-demo" />
        </fieldset>
      </label>

      <label>
        Range Slider
        <input type="range" />
      </label>

      <label>
        Progress element
        <progress max="100" value="50">50%</progress>
      </label>
      <p>src: https://codepen.io/web-dot-dev/pen/PomBZdy</p>
    </div>
    <hr />
  </section>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" module>
html {
  color-scheme: light dark;
}
.container {
  width: 300px;
}
label {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 4rem;
  & > input {
    accent-color: pink;
  }
}
fieldset {
  accent-color: pink;
  border: none;
  padding: 0;
}
progress {
  accent-color: #74992e;
}
</style>
