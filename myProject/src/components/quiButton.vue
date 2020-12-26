<template>
  <button class="qui-btn" v-on:click="btnClickEvent">
    <slot name="icon"></slot><!--重点在这里-->
    <span>{{msg}}</span>
  </button>
</template>

<script>
export default {
  props: {
    msg: {
      default: '下载'
    }
  },
  methods: {
    btnClickEvent: function () {
      alert('先弹出默认的文案')
      this.$emit('btnClickEvent')
    }
  }
}
</script>
<style scoped>
@import "../assets/css/reset.import.css";
@import "../assets/css/qui-btn.import.css";
</style>
