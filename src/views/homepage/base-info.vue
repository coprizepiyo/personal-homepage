<template>
  <div class="basic-information">
    <div class="basic-information-aside-left">
      <div class="bi-header">
        <p class="bi-name">{{basicInformation.name}}</p>
        <p class="bi-en-name">{{basicInformation.enName}}</p>
        <p class="bi-en-job">{{basicInformation.job}}</p>
        <p class="bi-en-job">{{basicInformation.enJob}}</p>
        <p class="bi-en-city">{{basicInformation.enCity}}</p>
      </div>
      <div class="bi-edu">
        <p class="bi-edu-title">EDUCATION</p>
        <p class="bi-edu-value">{{basicInformation.education}}</p>
      </div>
      <div class="bi-pro">
        <p class="bi-pro-title">PROFICIENCY</p>
        <ul class="bi-pro-list">
          <li class="bi-pro-item" v-for="item in proficiency">
            <p class="bi-pro-item-key">{{item.key}}</p>
            <p class="bi-pro-item-value">{{item.value}}</p>
          </li>
        </ul>
      </div>
    </div>
    <div class="basic-information-photo">
      <img src="../../assets/img/photo.jpg" />
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
        enJob: 'Web&Front End Engineer',
        education: '上海交通职业技术学院(大专)'
      },
      proficiency: [
        { key: 'Teamwork', value: 9 },
        { key: 'Creative', value: 8 },
        { key: 'Eye for the detail', value: 8 },
        { key: 'Communication', value: 8.5 }
      ]
    }
  }
}
</script>

<style>
.basic-information{
  width: 100%;
  height: 900px;
  position: relative;
  box-sizing: border-box;
  padding-right: 650px;
}

.basic-information-photo{
  width: 650px;
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
  margin: 110px 0 0 120px;
}

.bi-name{
  font-size: 46px;
  color: #1d1d1d;
}

.bi-en-name{
  font-size: 46px;
  color: #1d1d1d;
  margin-top: 5px;
}

.bi-en-job{
  font-size: 24px;
  margin-top: 15px;
  color: #1d1d1d;
}

.bi-en-city{
  font-size: 24px;
  margin-top: 10px;
  color: #bababa;
}

.bi-edu{
  margin: 200px 0 0 120px;
}

.bi-edu-title {
  font-size: 24px;
  color: #249cea;
}

.bi-edu-value {
  font-size: 20px;
  margin-top: 15px;
}

.bi-pro {
  margin: 80px 0 0 120px;
}

.bi-pro-title{
  font-size: 24px;
  color: #249cea;
}

.bi-pro-list{
  width: 100%;
  margin-top: 30px;
}

.bi-pro-item{
  float: left;
  text-align: center;
  width: 25%;
}

.bi-pro-item-key {
  font-size: 18px;
  color: #bababa;
}

.bi-pro-item-value {
  font-size: 75px;
  margin-top: 25px;
}

@media screen and (max-width: 414px) {
  .banner{
    width: 414px;
    height: 650px;
    background: url(../../assets/img/banner.jpg) center no-repeat;
    background-size: 1100px 650px;
  }

  .basic-information{
    width: 414px;
    height: 1400px;
    position: relative;
    padding-right: 0;
  }

  .basic-information-photo{
    width: 414px;
    left: 0;
    top: 0;
  }

  .basic-information-aside-left{
    position: absolute;
    width: 414px;
    height: 820px;
    top: 580px;
    padding-right: 20px;
    box-sizing: border-box;
  }

  .bi-header{
    margin: 20px 0 0 20px;
  }

  .bi-edu{
    margin: 80px 0 0 20px;
  }

  .bi-pro {
    margin: 80px 0 0 20px;
  }
  .bi-pro-item{
    float: left;
    text-align: center;
    width: 50%;
  }
}
</style>
