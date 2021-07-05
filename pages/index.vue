<template>
  <div class="section1 pt-10"> 
    <div style="position:relative">
      <div class="sectionTitle pb-1">COVID-19 Alert System</div>
      <div class="mx-3 sectionSubtitle" style="color:#fff">This system contains two applications:<br/> (1) Prediction of Covid-19 Infection and (2) Covid-19 Live Spatial Information Monitoring</div>
      <div class="d-flex mt-5">
        <div class="appBtn" @click="$router.push('/predict')">
          AI: The Prediction of Covid-19 Infection App
        </div>
        <div class="appBtn" @click="goToLink('http://169.51.203.30:31692')">
          GIS: Covid-19 Spatial Information Center
        </div>
      </div>
      <div style="position:relative">
        <div class="covImg">
          <img src="~assets/img/cov.png"/>
        </div>
        <div class="covImg" style="right:0;left:auto">
          <img src="~assets/img/cov.png"/>
        </div>
        <div class="covImg1" style="width:200px;transform:translateX(-50%);left:50%">
          <img src="~assets/img/cov.png"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  methods:{
    goToLink(url){
      window.open(url,"_blank")
    }
  }
}
</script>

<style lang="scss">
.section1 {
  background: rgb(20,84,138);
  background: radial-gradient(circle, rgba(20,84,138,1) 0%, rgba(32,76,134,1) 0%, rgba(0,0,0,1) 100%);
  min-height: 100vh;
  padding-bottom:100px;
  display:flex;
  justify-content: center;
  align-items: center;
  background-image:url('~assets/img/bg.jpg');
}

.sectionTitle {
  text-align: center;
  font-size:2.5em;
  color:#fff;
  font-weight:900;
  display:flex;
  justify-content: center;
  align-items: center;
  letter-spacing: -1px;
  line-height:1;
  background: rgb(38,156,255);
  background: linear-gradient(58deg, rgba(38,156,255,1) 0%, rgba(235,118,255,1) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  position:relative;
  z-index:10;
}

.sectionSubtitle {
  text-align: center;
  position:relative;
  z-index:10;
}

.covImg {
  img{
    width:100%;
    filter:opacity(70%);
  }
  width:150px;
  animation: MoveUpDown 10s linear infinite;
  position: absolute;
  left: 0;
  bottom: 0;
}

.covImg1 {
  img{
    width:100%;
    filter:opacity(80%);
  }
  width:150px;
   animation: MoveDownUp 10s linear infinite;
  position: absolute;
  left: 0;
  bottom: 0;
}

.appBtn {
  &:hover {
    color:#fff;
    background: rgb(38,156,255);
    background: linear-gradient(58deg, rgba(38,156,255,1) 0%, rgba(235,118,255,1) 100%);
    transform:scale(1.1);
  }
  transition:1s;
  position:relative;
  cursor:pointer;
  z-index:10;
  color:rgb(167,132,255);
  text-align: center;
  padding:30px;
  border:1px solid rgb(167,132,255);
  font-weight: bold;
  margin:0 10px;
  border-radius:10px;
  background-color:rgba(0,0,0,.5);
}

@keyframes MoveUpDown {
  0%, 100% {
    bottom: 0;
  }
  50% {
    bottom: 50px;
  }
}

@keyframes MoveDownUp {
  0%, 100% {
    bottom: 200px;
  }
  50% {
    bottom: 180px;
  }
}

</style>
