<template>
  <div id="pageQuiList">
    <qui-list tipsText="自定义文案，默认右边是按钮" msg="弹层"></qui-list>
    <qui-list v-on:btnClickEvent="test"></qui-list>
    <qui-list ref="child1" tipsText="最右边是箭头" currentView="qui-arrow"></qui-list>
  </div>
</template>

<script>
import quiList from './quiList'
export default {
  name: 'pageQuiList',
  components: {
    'qui-list': quiList
  },
  methods: {
    test: function () {
      alert('我是自定义的方法')
    }
  },
  beforeCreate: function () {},
  created: function () {},
  beforeMount: function () {},
  mounted: function () {
    console.log(this.$el)
    console.log(this.$children)
    console.log(this.$refs)
    console.log(this.$refs.child1.msg)
  },
  beforeUpdate: function () {},
  updated: function () {},
  beforeDestroy: function () {},
  destroyed: function () {}
}
</script>

<style scoped>

</style>
