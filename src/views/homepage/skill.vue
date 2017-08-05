<template>
  <div class="skill">
    <p class="skill-title">TECHNICIAL SKILLS</p>
    <ul class="skill-content fix">
      <li class="skill-item" v-for="row in skillList">
        <div class="skill-item-name"><span>{{row.name}}</span></div>
        <div class="skill-item-short">
          <div class="proficiency-continer" :style="{backgroundColor: row.color}">
            <div class="proficiency-cover" :style="{height: (100 - row.proficiency) * 160/100 + 'px'}"></div>
            <span>{{row.shortName}}</span>
          </div>
          
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      skillList: [
        {
          name: 'HTML&HTML5',
          shortName: 'HTML',
          proficiency: 0,
          color: '#005494'
        }, {
          name: 'CSS&CSS3',
          shortName: 'CSS',
          proficiency: 0,
          color: '#ff9c00'
        }, {
          name: 'Javascript&ES6',
          shortName: 'Js',
          proficiency: 0,
          color: '#d52959'
        }, {
          name: 'Vue',
          shortName: 'Vue',
          proficiency: 0,
          color: '#55bb00'
        }
      ],
      aProficiency: [85, 80, 85, 75]
    }
  },
  methods: {
    setProficiency () {
      for (let i = 0; i < this.skillList.length; i++) {
        this.skillList[i].proficiency = this.aProficiency[i]
      }
    },
    clearProficiency () {
      for (let i = 0; i < this.skillList.length; i++) {
        this.skillList[i].proficiency = 0
      }
    }
  },
  created () {
    var _this = this
    window.onscroll = function () {
      let scrollTop = document.body.scrollTop
      if (scrollTop > 1400) _this.setProficiency()
      else if (scrollTop < 900) _this.clearProficiency()
    }
  }
}
</script>

<style scoped>
.skill{
  padding: 100px 0 20px 120px;
}

.skill-title{
  font-size: 24px;
  color: #249cea;
}

.skill-item{
  float: left;
  width: 25%;
  min-width: 200px;
  padding-top: 80px;
}

.skill-item-name{
  width: 190px;
  font-size: 18px;
  text-align: center;
}

.skill-item-short{
  height:190px;
  width: 190px;
  border-radius: 95px;
  border: 2px solid #aaaaaa;
  margin-top: 50px;
  font-size: 24px;
  text-align: center;
}

.proficiency-continer {
  width: 160px;
  height: 160px;
  border-radius: 80px;
  margin: 15px;
  line-height: 160px;
  text-align: center;
  overflow: hidden;
}

.proficiency-cover {
  width: 100%;
  height: 100%;
  background-color: #fff;
  transition: 3s;
}

@media screen and (max-width: 414px) {
  .skill{
    padding: 100px 0 0 0;
    height: 1080px;
  }

  .skill-title{
    margin-left: 20px;
  }

  .skill-content {
    margin-left: 15px;
  }

  .skill-item{
    width: 50%;
    min-width: 190px;
  }

  .skill-item-short{
    height:180px;
    width: 180px;
    border-radius: 90px;
  }

  .proficiency-continer {
    width: 150px;
    height: 150px;
    border-radius: 75px;
    margin: 15px;
    line-height: 150px;
  }
}
</style>
