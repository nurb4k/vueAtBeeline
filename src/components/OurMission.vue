<template>
  <div class="mission">
    <div class="mission__image">
      <img alt="" :src="require('/src/assets/misson.png')">
    </div>
    <div class="mission__body">
      <div class="body__title"><p class="title">Наша миссия</p></div>
      <div class="body__description"><p class="description">Тебя тоже раздражает, когда ты пользуешься приложением или
        сайтом и непонятно куда нажать?<br> Когда попадаешь на пустой экран после ввода данных?
        <br><br>
        Нам тоже это не нравится!
        <br><br>
        Мы хотим улучшать наши продукты, делать их проще и удобнее для пользователя. Присоединяйся, без тебя нам не
        обойтись!</p></div>
      <div class="body__btn">
        <button class="btn">Присоединиться</button>
      </div>

    </div>
  </div>

</template>

<script>
export default {}
</script>

<style scoped lang="scss">
$fontColor: #10083F;
.mission {
  display: flex;
  width: 958px;
  height: 456px;
}

.mission__image {

  margin-right: 96px;
}

.mission__body {

}

.title {
  margin-bottom: 40px;
  color: $fontColor;
  font-size: 40px;
  font-weight: 700;
  line-height: 48px;
  text-align: left;
}

.description {
  text-align: left;
  margin-bottom: 55px;
  color: #504D64;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
}

.btn {
  width: 258px;
  height: 56px;
  background: #FFE14D;
  border-radius: 12px;
  border: none;
  color: $fontColor;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
}

@media only screen and (max-width: 376px) {
  .mission {
    width: 375px;
    height: 711px;
    display: flex;
    flex-direction: column-reverse;
  }

  .title {
    padding: 0 61px;
    font-size: 30px;
    font-weight: 700;
    line-height: 36px;
    letter-spacing: 0;
    text-align: center;
  }
  .mission__image img {
    height: 274px;
    width: 333px;
    margin-left: 42px;
    margin-bottom: 41px;

  }
  .body__description {
    width: 375px;
    height: 288px;
    margin-bottom: 24px;
    padding: 0 18px;
  }


  .body__description p {

    //margin-bottom: 24px;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 24px;
    display: flex;
    align-items: flex-end;
    text-align: center;
  }
  .body__btn {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .btn {
    height: 48px;
    margin-bottom: 48px;
  }

}
</style>