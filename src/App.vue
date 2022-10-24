<template>
  <div class="app">
    <div class="header">
      <header-content></header-content>
    </div>
    <div class="infoPanel">
      <info-panel></info-panel>
    </div>
    <div class="condition">
      <condition-component></condition-component>
    </div>
    <div class="ourMission">
      <our-mission></our-mission>
    </div>
  </div>
</template>

<script>


import HeaderContent from "@/components/HeaderContent";
import InfoPanel from "@/components/infoPanel";
import conditionComponent from "@/components/conditionComponent";
import OurMission from "@/components/OurMission";


export default {

  name: 'App',
  components: {
    InfoPanel,
    HeaderContent,
    conditionComponent,
    OurMission,
  },
}
</script>
<style lang="scss">


$fontColor: #10083F;
* {
  margin: 0;
  font-family: 'SF Pro Display', sans-serif;
  box-sizing: border-box;
}

.app {
  display: flex;
  flex-direction: column;
  position: relative;
  width: 100%;
}

.header {
  width: 1440px;
  height: 600px;
}

.condition {
  margin-left: 217px;
}

.ourMission {
  width: 1004px;
  margin-top: 123px;
  height: 600px;
  margin-left: 217px;
}

.infoPanel {
  width: 1004px;
  height: 1015px;
  margin-left: 217px;
  margin-right: 217px;
}

@media only screen and (max-width: 376px) {
  .header {
    width: 375px;
    height: 667px;
  }
  .infoPanel {
    width: 375px;
    height: 1498px;
    margin-left: 0;
    margin-right: 0;
    margin-bottom: 80px;
  }
  .condition {
    margin: 0;
    margin-bottom: -70px;
  }
  .ourMission {
    width: 375px;
    height: 711px;
    margin: 0;
  }
}
</style>
