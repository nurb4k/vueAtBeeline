<template>
  <div
      class="card"
      v-for="card in cards"
      :key="card.title"
      :style="card.backgroundColor"
  >
    <div class="card__photo-area">
      <img :src="require('/src/assets/'+card.image)">
    </div>
    <div class="card__title">
      <p>{{ card.title }}</p>
    </div>
    <p :style="card.backgroundColor" class="hidden">{{ card.description }}</p>
  </div>

</template>

<script>
export default {

  data() {
    return {
      cards: [
        {
          backgroundColor: "background-color:#FFF6CC;",

          image: 'img-1.png',
          title: "Будь первым",
          description: "Хочешь первым увидеть наши новые продукты и поучаствовать в их разработке?",
        },
        {
          backgroundColor: "background-color:#EAF4FF",

          image: "img2.png",
          title: "Поделись опытом",
          description: "Будем рады узнать о твоем опыте использования наших продуктов ",
        },
        {
          backgroundColor: "background-color: #000000;color:#FFFFFFB2;",
          image: "img3.png",
          title: "Будь первым",
          description: "Блестящая, свеженькая и такая уникальная ачивка в приложении “Мой Билайн” ",
        },
      ],

    }

  }


}
</script>

<style lang="scss">
.card {
  border-radius: 16px;
  margin-right: 28px;

  width: 33%;
  height: 100%;
  background-color: #EAF4FF;

  display: flex;
  flex-direction: column;

  &:hover {

    width: 361px;
    height: 441px;
    transition: all .6s;

    .card__photo-area {
      transition: all .6s;
      margin-top: 84px;
    }

    .card__title {
      transition: all .6s;
      margin-top: 12px;
    }

    .hidden {
      transition: all .6s;
      visibility: visible;
      margin-top: 12px;
      text-align: center;
      padding: 0 35px;
    }

  }


}


.card__photo-area {
  margin-top: 104px;
  /*margin-bottom: 207px;*/
  margin-left: 72px;
  margin-right: 71px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.card__title {
  /*margin-top: 36px;*/
  font-size: 20px;
  margin: 36px 28px 0 29px;
  font-weight: 500;
  line-height: 26px;
  text-align: center;
}

.hidden {
  visibility: hidden;
}

@media only screen and (max-width: 376px) {
  .card {
    width: 343px;
    height: 398px;
    margin: 12px 16px 12px 16px;

    pointer-events: none;

    &__photo-area {
      margin: 24px 96px 0 96px;
    }

    &__title {
      font-size: 20px;
      font-weight: 500;
      line-height: 26px;
      letter-spacing: 0;
      text-align: center;
      margin: 12px 26px;
    }

  }
  .hidden {
    visibility: visible;
    margin: 12px 25px 40px 25px;
    font-size: 18px;
    font-weight: 400;
    line-height: 24px;
    letter-spacing: 0;
    color: #00000080;

    text-align: center;

  }

}
</style>