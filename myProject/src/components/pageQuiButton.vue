<template>
  <div id="pageQuiButton">
    <!--使用-->
    <qui-btn msg="下载" class="with-icon">
      <img slot="icon" class="ico" src="xxx.png" />
    </qui-btn>
  </div>
</template>
<script>
import quiBtn from './quiButton'
export default {
  name: 'pageQuiButton',
  components: {
    'qui-btn': quiBtn
  },
  methods: {
    doSth: function () {
      alert('你点击了组件的click:btnClickEvent')
    }
  }
}
</script>
