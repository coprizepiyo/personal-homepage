<template>
  <div>
    <div class="banner"></div>
    <div class="basic-information">
      <div class="basic-information-aside-left">
        <div class="bi-header">
          <p class="bi-name">{{basicInformation.name}}</p>
          <p class="bi-en-name">{{basicInformation.enName}}</p>
          <p class="bi-en-job">{{basicInformation.enJob}}</p>
          <p class="bi-en-city">{{basicInformation.enCity}}</p>
        </div>
        <div class="bi-content">
          <p class="bi-content-title">基本资料 <span style="margin-left: 20px;">basic info</span></p>
        </div>
      </div>
      <div class="basic-information-photo">
        <img src="../../assets/img/photo.jpg" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      basicInformation: {
        name: '连炜',
        enName: 'Coprize Piyo',
        Gender: '男',
        birthday: '1986-03-23',
        city: '上海',
        enCity: 'City Shanghai',
        job: '前端工程师',
        enJob: 'Web&Front End Engineer'
      }
    }
  }
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

.bi-header{
  margin: 80px 0 0 120px;
}

.bi-name{
  font-size: 46px;
}

.bi-en-name{
  font-size: 46px;
}

.bi-en-job{
  margin-top: 10px;
}

.bi-en-city{
  margin-top: 10px;
  color: #bababa;
}

.bi-content{
  margin: 50px 0 0 120px;
}

.bi-content-title {
  color: #249cea;
}
</style>
