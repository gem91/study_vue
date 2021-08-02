<template>
  <header>
    <a class="logo" href="#"><img src="../assets/youtube-logo.png" alt="유튜브 로고"></a>
    <input v-model="searchVideo" v-on:keyup.enter="findBtn" class="text-search" type="search" placeholder="search..." >
    <button class="btn-search" v-on:click="findBtn"><i class="fas fa-search"></i></button>
  </header>
</template>

<script>
export default {
  data: function(){
    return {
      searchVideo: "",
    }
  },
  methods: {
    findBtn: function(){
      console.log(this.searchVideo);
      this.clearInput();
    },
    clearInput: function(){
    this.searchVideo = '';
    }
  }
}
</script>

<style scoped>
  header{ padding: 20px 30px; margin: 0 auto;  background: #222;}
  .logo{ margin-right: 150px; display: inline-block; width: 150px;}
  .logo img{ width: 100%;}
  .text-search{display: inline-block; margin-top: 5px; padding: 7px 15px; width: calc(100% - 550px); vertical-align: top; border-radius: 3px; border: 0;}
  .btn-search{ margin-left: 1px; margin-top: 4px; padding: 8px 20px; border-radius: 2px; background: red; vertical-align: top;}
  .fa-search{ color: #fff}
</style>