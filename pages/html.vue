<template>
  <div style="padding: 50px">
    <h2>HTML</h2>
    <section :class="$style.container">
      <h3>&lt;dialog&gt;&lt;/dialog&gt;</h3>
      <p>考慮することが多い</p>
      <p>・背景backdropの設定</p>
      <p>・スクロールブロック対応</p>
      <p>
        ・キーボード操作時: Tabがdialog内部だけを移動するよう制御、Escで閉じる
      </p>
      <p>○Interop 2022</p>
      <p>https://wpt.fyi/interop-2022</p>
      <button @click="openModal()">! OPEN !</button>
      <button>他のボタン</button>
      <button>他のボタン</button>
      <button>他のボタン</button>
      <dialog ref="modal" :class="$style.modal">
        <button @click="closeModal()">x</button>
        <h2>開いたダイアログ</h2>
        <p>
          コンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツコンテンツ
        </p>
      </dialog>
    </section>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      modal:"",
    }
  },
  methods: {
    openModal() {
      if (typeof this.$refs.modal !== "undefined") {
        this.$refs.modal.showModal()
      }
    },
    closeModal() {
      if (typeof this.$refs.modal !== "undefined") {
        this.$refs.modal.close()
      }
    },
  },
})
</script>

<style lang="scss" module>
.modal {
  margin-top: 30px;
  padding: 20px;
  width: 300px;
  border-radius: 8px;
  &::backdrop {
    background-color: rgba(0, 0, 0, 0.3);
  }
}
</style>
