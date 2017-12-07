<template>
  <tab :tab-list="tabList" v-model="selected">
    <div id="tab1" v-show="selected ==='tab1'">tab 11111</div>
    <div id="tab1" v-show="selected ==='tab2'">tab  2</div>
  </tab>
</template>
<script>
  export default {
    data () {
      return {
        tabList: ['tab1', 'tab2'],
        selected: 'tab1'
      }
    }
  }
</script>
