<template>
    <div class="border-top border-success">
      <ul class="border-top">
        <li v-for="gif in gifs">
          <img :src="gif.images.fixed_height.url" />
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    props: [ 'gifs' ]
  }
  </script>
  
  <style>
    li {
      list-style: none;
      float: left;
      margin: 20px;
    }
  </style>