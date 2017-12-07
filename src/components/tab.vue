<template>
  <div>
    <ul class="tabs">
      <li class="li-tab" v-for="(item,index) in tabsParam" @click="toggleTabs(index)" :class="{active:index!=nowIndex}" :key="index">{{item}}</li>
    </ul>
    <div class="divTab" v-show="nowIndex===0">我是tab1</div>
    <div class="divTab" v-show="nowIndex===1">我是tab2</div>
  </div>
</template>
<script>
export default {
  data(){
    return {
      tabsParam: ['tab1',"tab2"],
      nowIndex: 0
    }
  },
  methods: {
    toggleTabs(index) {
      this.nowIndex = index
    }
  },
  watch: {
    value(val){
      this.currentActive = val ;
    }
  }
}
</script>
