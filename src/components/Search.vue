<template>
    <div class="search">
      <nav class="navbar navbar-expand-lg navbar-light bg-light justify-content-center">
        <a class="navbar-brand" href="#">Giphy Gifs with <span class="text-success">Vue</span></a>
          <input type="text" v-model="query" @keypress.enter="handleSearch" placeholder="search your favourite gif !" />
          <button type="button" class="btn btn-outline-success ml-2" @click="handleSearch">Search</button> 
      </nav>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        query: ''
      }
    },
    methods: {
      handleSearch() {
        this.$emit('SearchRequested', this.query);
      }
    }
  }
  </script>
  
  
  <style>
    .search input {
      padding: 10px 20px;
      border: 1px solid #CCC;
      border-radius: 5px;
      width: 400px;
    }
    .search button {
      padding: 5px 15px;
      border: 1px solid #CCC;
      background-color: #4183c4;
      color: #FFF;
      font-size: 16px;
      border-radius: 5px;
    }
  </style>
  