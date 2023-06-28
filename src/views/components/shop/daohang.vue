<template>
  <div class="daohang-body">
    <div class="daohang-body-left">
      <h5>分类</h5>

    </div>
    <div class="daohang-body-mid">1</div>
<!--    <div class="daohang-body-right">1</div>-->
  </div>
</template>

<script>
    export default {
        name: "daohang"
    }
</script>

<style scoped>
  .daohang-body{
    display: flex;
    height: 300px;
    padding: 10px 10px 10px 10px;
    border-radius: 10px;
  }
  .daohang-body-left{
    flex: 2;
    background-color: rgb(231, 228, 229);
    border-radius: 10px;
    margin-right: 10px;
  }
  .daohang-body-mid{
    flex: 4;
    background-color: rgb(231, 228, 229);
    border-radius: 10px;
    margin-right: 10px;
  }
  /*.daohang-body-right{*/
  /*  flex: 2;*/
  /*  background-color: rgb(231, 228, 229);*/
  /*  border-radius: 10px;*/

  /*}*/
</style>
