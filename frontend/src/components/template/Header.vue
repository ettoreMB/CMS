<template>
  <header class="header">
    <a class="toogle">
      <i class="fa fa-lg"></i>
    </a>

    <h1 class="title">
       {{title}}
    </h1>

  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
     title: String, 
     hideToogle: Boolean, 

  }
}
</script>

<style>
  .header {
    grid-area: header;
    background: #1e469a;
    display: flex;
    justify-content: center;
    align-items: center;
    
  }
</style>