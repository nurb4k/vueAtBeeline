<template>
  <div id="header" class="header">
    <div class="header__head " id="header__head">
      <div class="header__head-beeline-icon">
        <img alt="" class="beeline-icon" :src="require('/src/assets/beeline_icon.png')"/>
      </div>
      <input type="checkbox" id="check">
      <label for="check" class="checkbtn">
        <img :src="require('/src/assets/nav-icon.png')" alt="navbar icon">
      </label>
      <ul class="head__li">
        <li><a href="#"> Какие плюсы? </a></li>
        <li><a href="#">Как принять участие?</a></li>
        <li><a href="#">Наша миссия</a></li>
        <li><a href="#">Присоединиться</a></li>
      </ul>
    </div>
    <div class="header__body">
      <div class="body-text">
        <div class="body-text__title"><p>Стань нашим
          респондентом</p>
        </div>
        <div class="body-text__description">Мы хотим услышать твое мнение, опыт
          и боли общения с цифровыми продуктами Beeline.
        </div>
        <div class="body-text__btns">
          <a href="https://docs.google.com/forms/d/e/1FAIpQLSfm_Yj07urIb_fF0mTRGZgl5DWt5lC2qYd4TngwXWMgMHiYMg/viewform?usp=sf_link"
             class="body-text__btn">Я готов!</a>
        </div>
      </div>
      <div class="body-image">
        <img alt="" class="body-image__image" :src="require('/src/assets/Group.png')">
      </div>
    </div>
  </div>

</template>

<script>
export default {
  methods: {
    navbar() {
      var x = document.getElementById("header");
      if (x.className === "header") {
        x.className += " responsive";
      } else {
        x.className = "header";
      }
    }
  }

}
</script>

<style scoped lang="scss">
$color: #DDEFFF;
$fontColor: #10083F;

.header {
  padding: 42px 221px 42px 217px;
  background-color: $color;

}

/*  NAVBAR   */
.header__head {

  display: flex;
  flex-direction: row;

  align-items: center;
  width: 100%;
  height: 70px;
}

.header__head-beeline-icon {
  padding-right: 180px;
}

.header__head-beeline {

  display: flex;
  width: 25%;
}

.beeline-icon {
  margin: 0;
  width: 36px;
  height: 36px;
}

.head__li {
  float: right;
  display: flex;
  justify-content: center;
  align-items: center;

  & > * {


  }

  & li {

    display: inline-block;
    margin: 0 18px;

    & > a {

      font-size: 16px;
      font-weight: 700;
      color: $fontColor;
      line-height: 22px;
      letter-spacing: 0;
      text-align: left;

      text-decoration: none;

    }
  }

}

.checkbtn {
  float: right;
  line-height: 80px;
  cursor: pointer;
  display: none;
}

#check {
  display: none;
}


/* end navbar */


.header__body {

  width: 100%;
  display: flex;
  align-items: center;
}


.body-text__title {
  padding-bottom: 24px;
  font-size: 40px;
  font-weight: 700;
  color: $fontColor;
  line-height: 48px;

}

.body-text {
  display: flex;
  flex-direction: column;
}

.body-text__btns {
  display: flex;
  flex-direction: column;
  width: 130px;

}

.body-text__btn {
  text-decoration: none;
  border-radius: 12px;
  border: none;
  padding: 14px;
  background-color: #FFE14D;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  text-align: center;
  width: 160px;
  height: 56px;
}

.body-text__description {
  padding-bottom: 24px;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
}

.body-image {
  padding-bottom: 36px;
}


@media only screen and (max-width: 376px) {
  .checkbtn {
    height: 36px;
    width: 36px;
    display: block;

  }
  #check:checked ~ ul {
    left: 0;
  }
  .beeline-icon {
    height: 40px;
    padding-top: 4px;
  }
  .checkbtn img{
    padding-bottom: 9px;
  }
  ul {
    position: fixed;
    width: 100vh;
    height: 100vh;
    background-color: #DDEFFF;
    top: 80px;
    left: -100%;
    text-align: center;

    transition: all .5s;
  }
  .head__li {
    width: 375px;
    padding: 0;
    display: flex;
    flex-direction: column;

    & li {
      color: $fontColor;
      font-size: 24px;
      font-weight: 700;
      line-height: 32px;
      letter-spacing: 0px;
      text-align: left;

      display: block;
    }
  }

  .header {
    width: 375px;
    height: 667px;
    display: flex;
    flex-direction: column;
    padding: 28px 20px 0 20px;
  }


  .header__head-beeline {
    width: 36px;
    height: 36px;
  }

  .header__head {

    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 36px;
  }


  .header__body {
    width: 100%;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }


  .body-text__title {

    font-size: 30px;
    font-weight: 700;
    line-height: 36px;
    padding-bottom: 12px;
    text-align: center;


  }
  .body-text__description {
    height: 96px;
    width: 376px;
    padding-left: 38px;
    padding-right: 38px;
    align-items: center;
    align-content: center;
    font-size: 18px;
    font-weight: 400;
    line-height: 24px;

    text-align: center;

  }

  .body-text {
    margin-top: 48px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .body-text__btn {
    height: 48px;
  }
  .body-image__image {
    margin-top: 59px;
    width: 354px;
    height: 235px;
  }


}

</style>