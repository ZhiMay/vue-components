<template>
 <div class="tabs">
   <div class="tabs-bar">
     <div class="tabs-tab" v-for="(tab,index) in tabList" :class="[currentIndex == tab ? 'tab-active' : '']" :key="index" @click="changeTab(tab)">
       {{tab}}
     </div>
   </div>
   <div class="tabs-content">
     <slot></slot>
   </div>
 </div>
</template>



<script>
export default {
  props: {
    tabList: Array,
    vaule: {}
  },
  data(){
    return {
      currentIndex: this.vaule
    }
  },
  methods: {
    changeTab(vaule) {
      this.currentIndex = vaule
    }
  },
  watch: {
    value(val){
      this.currentActive = val
    },
    currentIndex(val,oldVal){
      this.$emit('input',val)
    }
  }
}
</script>
<style>
 .tabs-bar{
   background:#f5f6f7;
 }
 .tabs-tab{
   display: inline-block;
   width: 50%;
   text-align: center;
   height: 50px;
   line-height: 50px;
   cursor: pointer;
 }
 .tab-active{
   color:red;
 }
</style>

