<template>
  <div class="sale-reports">
    <div class="header"></div>
    <div class="content"></div>
    <div class="footer"></div>
  </div>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.sale-reports {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  background-color: #fff;
  box-shadow: 0 2px 8px rgba(4, 5, 9, .7);
  .header {
    width: 100%;
    height: 50px;
    border-bottom: 1px solid #ccc;
    box-sizing: border-box;
    // background-color: red;
  }
  .content {
    flex: 1;
    width: 100%;
    // background-color: green;
  }
  .footer {
    width: 100%;
    height: 120px;
    border-top: 1px solid #ccc;
    box-sizing: border-box;
    // background-color: blue;
  }

}
  
</style>