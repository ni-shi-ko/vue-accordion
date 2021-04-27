<template>
  <div id="app">
     <div id="accordion">
       <button @click="accordionClick">アコーディオン</button>
     </div>
     <div class="inner" v-if="isOpen">アコーディオンの中身が入ります</div>
  </div>
</template>

<script>
  export default {
    data() {
     return {
       isOpen: false
     };
    },
    methods: {
      accordionClick() {
        this.isOpen = !this.isOpen;
      }
    }
  }
</script>

<style>
  #accordion {
    width: 40%;
  }
  button {
    width: 100%;
    padding:1rem ;
    text-align: left;
  }
  .inner {
    width: 40%;
    padding: 16px 0;
  }
</style>
