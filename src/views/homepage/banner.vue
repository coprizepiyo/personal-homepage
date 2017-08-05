<template>
  <div class="banner"></div>
</template>

<script>
export default {
}
</script>

<style scoped>
.banner{
  width: 100%;
  height: 1080px;
  background: url(../../assets/img/banner.jpg) no-repeat center;
}

@media screen and (max-width: 414px) {
  .banner{
    width: 414px;
    height: 650px;
    background: url(../../assets/img/banner.jpg) center no-repeat;
    background-size: 1100px 650px;
  }
}

</style>
