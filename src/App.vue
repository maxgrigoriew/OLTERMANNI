<template>
  <header class="header">
    <div class="container">
      <div class="header__inner">
        <div class="logo"><img src="./assets/images/icons/logo.svg" alt="Логотип" /></div>
        <nav class="menu">
          <ul class="menu__list">
            <li class="menu__item"><a href="#" class="menu__link">Правила</a></li>
            <li class="menu__item"><a href="#" class="menu__link">Призы</a></li>
            <li class="menu__item"><a href="#" class="menu__link">Победители</a></li>
          </ul>
        </nav>
        <div class="menu__buttons">
          <button class="button menu__button">Вход</button
          ><button class="button menu__button outline">Регистрация</button>
        </div>
      </div>
    </div>
    <RouterView />
  </header>
  <main class="main">
    <section class="section promo">
      <div class="promo__img">
        <div class="container promo__img-container">
          <img class="promo__img-man" src="./assets/images/man.png" alt="man" />
        </div>
        <img class="promo__img-background" src="./assets/images/promo.png" alt="Promo" />
      </div>
      <div class="container">
        <div class="promo__inner">
          <button class="button promo__button">Загрузить чек</button>
          <p class="promo__text">Нам 40 лет — вам подарки</p>
          <ul class="promo__list">
            <li class="promo__list-item">
              <img src="./assets/images/icons/cart.svg" alt="Иконка" class="promo__list-img" />
              <p class="promo__list-text">
                Покупайте сыр <br />
                Oltermanni
              </p>
            </li>
            <li class="promo__list-item">
              <img src="./assets/images/icons/laptop.svg" alt="Иконка" class="promo__list-img" />
              <p class="promo__list-text">
                Регистрируйте чеки на сайте в период с 1 сентября по 30 ноября 2020 года
              </p>
            </li>
            <li class="promo__list-item">
              <img src="./assets/images/icons/phone.svg" alt="Иконка" class="promo__list-img" />
              <p class="promo__list-text">Получайте гарантированные призы — деньги на телефон</p>
            </li>
            <li class="promo__list-item">
              <img src="./assets/images/icons/best.svg" alt="Иконка" class="promo__list-img" />
              <p class="promo__list-text">Участвуйте в еженедельных розыгрышах</p>
            </li>
            <li class="promo__list-item">
              <img src="./assets/images/icons/card.svg" alt="Иконка" class="promo__list-img" />
              <p class="promo__list-text">
                Получите возможность выиграть 400 000 ₽ на новый интерьер
              </p>
            </li>
          </ul>
        </div>
      </div>
    </section>
  </main>
</template><style lang="scss">
@import './assets/scss/vars';

.header {
  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-height: 76px;
  }
}

.menu {
  &__list {
    display: flex;
    align-items: center;
  }

  &__item {
    padding: 0 10px;
  }

  &__item:not(:last-child) {
    margin-right: 42px;
  }

  &__link {
    color: $accent-color;
    font-weight: 500;
    font-size: 16px;
    text-transform: uppercase;
  }

  &__button {
    font-size: 16px;
  }

  &__button:not(:last-child) {
    margin-right: 17px;
  }
}

.button {
  cursor: pointer;
  padding: 10px 42px;
  border-radius: 20px;
  border: none;
  text-transform: uppercase;
  background: $yellow-color;
  color: $accent-color;
}

.button.outline {
  cursor: pointer;
  border: none;
  text-transform: uppercase;
  background: transparent;
  padding: 0;
}

@media (max-width: 767px) {
  .header {
    &__inner {
      min-height: 62px;
    }
  }

  .button.outline {
    display: none;
  }

  .menu {
    display: none;
  }
}
</style>