<template>
  <div class="info-panel">
    <div class="info-panel__title">
      <p class="title">Кто такой респондент?</p>
    </div>
    <div class="info-panel__body-text">
      <p class="body-text">Респондент - человек, принимающий участие в опросе, интервью или тестировании дизайна. Мы
        используем твои
        ответы в проектировании новых продуктов, чтобы сделать их понятнее, удобнее и приятнее для пользователей.</p>
    </div>
    <div class="info-panel__card-area">
      <div class="info-panel__title">
        <p class="title-card">Какие плюсы?</p>
      </div>
      <div class="info-panel__card">
        <card-component></card-component>
      </div>
    </div>
  </div>
</template>

<script>
import cardComponent from "@/components/cardComponent";

export default {
  components: {
    cardComponent,
  }
}
</script>

<style lang="scss">
$fontColor: #10083F;

.info-panel {
  margin-top: 110px;
  width: 100%;
  height: 300px;
  display: flex;
  flex-direction: column;
}

.title {
  color: $fontColor;
  font-weight: 700;
  font-size: 40px;
  line-height: 48px;
  text-align: center;
}

.info-panel__body-text {
  margin-top: 36px;
  display: flex;
  color: $fontColor;
  justify-content: center;
  align-items: center;
}

.body-text {
  width: 642px;
  height: 72px;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  text-align: center;
}

.title-card {
  font-size: 40px;
  margin-bottom: 40px;
  line-height: 48px;
  font-weight: 700;
  color: $fontColor;
}

.info-panel__card {
  display: flex;
  flex-direction: row;
  width: 1003px;
  height: 441px;
}

.info-panel__card-area {
  margin-top: 110px;
}

@media only screen and (max-width: 376px) {

  .info-panel {
    margin-top: 64px;
    width: 375px;
    height: 667px;
    display: flex;
    flex-direction: column;
  }
  .title {
    padding: 0 67px;
    font-size: 30px;
    font-weight: 700;
    line-height: 36px;
    letter-spacing: 0;
    text-align: center;
    color: $fontColor;
  }
  .info-panel__body-text {
    width: 100%;
    margin-top: 12px;
    margin-bottom: 32px;
    padding: 0 27px;
    display: flex;
  }
  .body-text {
    width: 322px;
    font-size: 18px;
    height: 210px;
    font-weight: 400;
    line-height: 24px;
    letter-spacing: 0;
    text-align: justify;
    align-items: center;
    color: #504D64;
  }
  .title-card {
    margin-bottom: 24px;
    font-size: 30px;
    font-weight: 700;
    line-height: 36px;
    letter-spacing: 0;
    text-align: center;
  }
  .info-panel__card-area {
    margin-top: 0;
    height: 1082px;
    width: 375px;


  }
  .info-panel__card {
    height: 1082px;
    width: 375px;
    display: flex;

    flex-direction: column;


    &:first-child(:last-child) {
      .hidden {
        color: red;
      }

    }
  }


}

</style>
