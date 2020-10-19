<template>
  <div class="card">
    <a class="card__avatar">
      <img
        class="card__img"
        src="https://via.placeholder.com/190x220.jpg"
        alt=""
      />
    </a>
    <div class="card__achievements">
      <div class="card__achievement">
        <span class="card__achievement-num">12</span>
        <span class="card__achievement-text">стаж</span>
      </div>
      <div class="card__achievement">
        <span class="card__achievement-num">6</span>
        <span class="card__achievement-text">консультаций</span>
      </div>
      <div class="card__achievement">
        <span class="card__achievement-num">1</span>
        <span class="card__achievement-text">отзывов</span>
      </div>
    </div>

    <h4 class="card__name">
      <a class="card__name-link" href="#">Виталий Вакулинский</a>
    </h4>
    <div class="card__details">
      <span>Психолог.</span> <span>1 год, 3 месяца на сайте,</span>
      <span>был 21 день назад</span>
    </div>
    <p class="card__story">
      Практикующий семейный психолог с опытом работы более 10 лет. Основную
      консультативную работу веду с супружескими парами. Часто бывает инициатива
      начинается...
    </p>
    <div class="card__price">
      <h5 class="card__price-title">Стоимость консультации</h5>
      <div class="card__price-details">
        <div class="card__price-item">1500 ₽</div>
        <div class="card__price-item">1500 ₽</div>
      </div>
    </div>
    <div class="card__tags">
      <span class="card__tag">вина</span>
      <span class="card__tag">кризисы</span>
      <span class="card__tag">личные границы</span>
      <span class="card__tag">поиск себя</span>
      <span class="card__tag">самооценка</span>
    </div>
    <div class="card__info">Уже обратилось: 1 клиентов</div>
  </div>
</template>

<script>
export default {
  name: 'Card',
}
</script>

<style scoped lang="scss">
.card {
  box-sizing: border-box;
  padding: 3.5rem 3rem;
  background: #fff;
  border-radius: 0.3rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.08);
  margin-bottom: 4rem;
  overflow: hidden;
  flex-wrap: wrap;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-start;
  min-height: 33.5rem;
}

.card__avatar {
  width: 19rem;
  position: absolute;
  top: 3.5rem;
  left: 3rem;
  height: 22rem;
}
.card__img {
  object-fit: cover;
}
.card__achievements {
  display: flex;
  width: 19rem;
  height: 4.5rem;
  justify-content: space-between;
  align-items: flex-end;
  position: absolute;
  top: 26rem;
  left: 3rem;
}
.card__achievement {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.card__achievement-num {
  font-size: 1.6rem;
  font-weight: 700;
  color: #595959;
}
.card__achievement-text {
  font-size: 1rem;
  font-weight: 700;
  line-height: 1;
  color: #90a4ae;
}

.card__name {
  margin: 0;
  line-height: 1;
  font-size: 1.8rem;
  width: calc(100% - 24rem);
}
.card__name-link {
  color: #0fc1a7;
  text-decoration: none;
}
.card__details {
  font-size: 1.1rem;
  color: #90a4ae;
  width: calc(100% - 24rem);
}
.card__story {
  margin: 1.5rem 0;
  font-size: 1.4rem;
  width: calc(100% - 24rem);
}
.card__price {
  margin-bottom: 1rem;
  width: calc(100% - 24rem);
}
.card__price-details {
  display: flex;
  color: #546e7a;
  font-size: 1.4rem;
  line-height: 1.54rem;
  font-weight: 700;
}
.card__price-title {
  margin-bottom: 1.1rem;
  color: #546e7a;
  font-size: 1.4rem;
  font-weight: 700;
  line-height: 2.1rem;
}
.card__price-item {
  display: flex;
  align-items: center;
  margin-right: 0.9rem;
  &::before {
    display: block;
    content: '';
    width: 2.4rem;
    height: 2.4rem;
    margin-right: 1.1rem;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='%23546e7a' id='i-round-textsms' viewBox='0 0 24 24'%3E%3Cpath d='M20,4H4C2.9,4,2.01,4.9,2.01,6L2,24l4-4h14c1.1,0,2-0.9,2-2V6C22,4.9,21.1,4,20,4z M9,13H7v-2h2V13z M13,13h-2v-2h2V13z M17,13h-2v-2h2V13z'%3E%3C/path%3E%3C/svg%3E");
  }
}

.card__tags {
  display: flex;
  flex-wrap: wrap;
  width: calc(100% - 24rem);
}
.card__tag {
  display: inline-block;
  background: #f5f3f7;
  color: #807987;
  font-size: 1.3rem;
  margin: 0 0.3rem 1rem;
  padding: 0.3rem 1rem;
  border-radius: 0.5rem;
}
.card__info {
  width: calc(100% - 24rem);
}

@media (max-width: 1000px) {
  .card {
    max-width: 100%;
  }
}

@media (max-width: 560px) {
  .card {
    position: relative;
    flex-direction: row;
    align-items: flex-start;
  }
  .card__avatar {
    width: 7rem;
    height: 7rem;
    overflow: hidden;
    border-radius: 50%;
    position: static;
    order: 1;
  }
  .card__name {
    order: 2;
    width: calc(100% - 16rem);
    margin-left: 8rem;
    position: absolute;
  }
  .card__details {
    order: 3;
    width: calc(100% - 16rem);
    position: absolute;
    margin-top: 2rem;
    margin-left: 8rem;
  }
  .card__story {
    position: absolute;
    order: 4;
    width: calc(100% - 16rem);
    margin-top: 4rem;
    margin-left: 8rem;
    overflow: hidden;
    height: 9rem;
  }
  .card__achievements {
    position: static;
    order: 5;
    width: 100%;
    margin-top: 8rem;
    margin-bottom: 2.2rem;
    border-top: 0.1rem solid #eceff1;
    border-bottom: 0.1rem solid #eceff1;
    padding-top: 0.7rem;
    padding-bottom: 1rem;
    height: 5rem;
  }
  .card__price {
    width: 100%;
    order: 6;
    margin-bottom: 2rem;
  }
  .card__tags {
    width: 100%;
    order: 7;
    margin-bottom: 2rem;
  }
  .card__info {
    order: 8;
    width: 100%;
  }
  .card__img {
    width: 100%;
    object-position: center;
  }
}
</style>
