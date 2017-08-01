<template>
  <div>
    <div class="banner"></div>
    <div class="basic-information">
      <div class="basic-information-aside-left">123</div>
      <div class="basic-information-photo">
        <img src="../../assets/img/photo.jpg" />
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.banner{
  width: 100%;
  height: 1080px;
  background: url(../../assets/img/banner.jpg) no-repeat center;
}

.basic-information{
  width: 100%;
  height: 900px;
  position: relative;
  box-sizing: border-box;
  padding-right: 500px;
}

.basic-information-photo{
  width: 500px;
  position: absolute;
  right:0;
}

.basic-information-photo img {
  display: block;
  width: 100%;
}

.basic-information-aside-left{
  float: left;
  width: 100%;
  height: 100%;
}
</style>
