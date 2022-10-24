<template>
  <div class="conditions">
    <div class="conditions__header_text">
      <p class="condition__title">Как принять участие?</p>
    </div>
    <div class="conditions__body">
      <div class="condition__card"
           v-for="card in cards"
           :key="card.title"
      >
        <div class="card__btn-number" :style="card.backgroundColor">
          {{ card.number }}
        </div>
        <div class="card__title-text">
          {{ card.title }}
        </div>
        <div class="card__description">
          {{ card.description }}
        </div>
      </div>
    </div>

  </div>

</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          number: 1,
          backgroundColor: "background-color:#FFF6CC;color:#0183D4",
          title: "Оставь заявку",
          description: "Заполни форму максимально честно, выбери продукты которые хочешь тестировать",
        },
        {
          number: 2,
          backgroundColor: "background-color:#F3ECFF; color:#9E66FF",
          title: "Ожидай приглашения на интервью",
          description: "Будь на связи :) Мы напишем тебе заранее и договоримся об удобном времени. Обычно интервью не занимает больше 30-40 минут. ",
        },
        {

          number: 3,
          backgroundColor: "background-color: #DFF6D9 ;color:#61CA45",
          title: "Позаботься об окружении",
          description: "Выбери спокойное, тихое место с хорошим интернетом. Обязательно приноси с собой хорошее настроение😉",
        },
        {

          number: 4,
          backgroundColor: "background-color: #FFF7E2;color:#FFBD12",
          title: "Получи клевую ачивку",
          description: "После первого интервью, в приложении\n" +
              "Мой Билайн тебе откроется новая ачивка\n" +
              "«Яркий пиздюк». Спасибо, что ты с нами!\n",
        },
      ],
    }
  }
}
</script>

<style scoped lang="scss">


.condition__title {
  color: #10083F;
  text-align: center;
  font-size: 40px;
  line-height: 48px;
  font-weight: 700;
}

.conditions__header_text {
  margin-top: 20px;
  margin-bottom: 40px;
}

.conditions__body {
  flex-wrap: wrap;
  width: 958px;
  height: 496px;

  display: flex;

}

.condition__card {
  display: flex;
  margin-right: 79px;
  flex-direction: column;
  width: 400px;
  height: 200px;


}

.card__btn-number {
  align-items: center;
  margin-bottom: 24px;
  width: 62px;
  height: 62px;
  display: flex;
  justify-content: center;
  border-radius: 16px;
  font-size: 36px;
  font-weight: 700;
  line-height: 26px;
  text-align: center;
}

.card__title-text {

  margin-bottom: 12px;
  font-size: 20px;
  font-weight: 500;
  line-height: 26px;
  text-align: center;
}

.card__description {
  font-size: 18px;
  font-weight: 400;
  line-height: 24px;
  text-align: left;
  color: #858295;
}

@media only screen and (max-width: 376px) {
  .conditions__header_text {
    font-size: 30px;
    font-weight: 700;
    line-height: 36px;
    letter-spacing: 0;
    text-align: center;
    margin-top: 80px;
    margin-bottom: 24px;
  }
  .conditions__body {
    display: flex;
    flex-direction: column;
    width: 375px;
    margin: 0;
    height: 1140px;
  }
  .condition__card {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 40px;
    margin-right: 0;
    padding: 0 36px;
  }
  .card__btn-number {
    width: 62px;
    min-height: 62px;
    margin-bottom: 20px;
  }

  .card__title-text {
    font-size: 20px;
    font-weight: 500;
    line-height: 26px;
    letter-spacing: 0;
    color: #000000;
    text-align: center;
  }
  .card__description {
    text-align: center;
    font-size: 18px;
    font-weight: 400;
    line-height: 24px;
    letter-spacing: 0px;
    max-width: 303px;
  }

}

</style>