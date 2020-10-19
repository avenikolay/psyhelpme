<template>
  <section class="content">
    <div class="container">
      <h1 class="main-title">500+ дипломированных психологов</h1>
      <h5 class="main-subtitle">
        Наши психологи помогут справиться с тревогой, депрессией, разобраться в
        личных отношениях и найти в себе ресурсы для решения любого вашего
        вопроса. Получите консультацию прямо сейчас.. Консультации психологов:
        переживание одиночества, неуверенности, неприятия себя, утраты, насилия,
        стресса, отсутствия смысла жизни и пр., а также - по вопросам
        самопознания и саморазвития
      </h5>
      <Sort />
      <div class="cols">
        <div class="cols__cards">
          <Card />
          <Card />
          <Card />
        </div>
        <div class="cols__filters">
          <Filters />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import Sort from '~/components/Sort'
import Card from '~/components/Card'
import Filters from '~/components/Filters'
export default {
  components: { Filters, Card, Sort },
}
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  font-family: Roboto, Arial, sans-serif;
  font-size: 10px;
}
body {
  background: #f5f7fb;
  line-height: 1.5;
  font-size: 1.5rem;
  font-weight: 400;
  color: #5f6368;
  display: flex;
  flex-direction: column;
}
.container {
  color: #000;
  padding: 6rem 4rem 8rem;
  max-width: 1300px;
  margin: 0 auto;
}
.main-title {
  margin: 5.1rem 0 4rem;
  line-height: 1.3;
  font-size: 2.3rem;
}
.main-subtitle {
  margin: 0 0 1rem;
  padding-left: 0.1rem;
  font-size: 1.3rem;
  font-weight: 400;
  color: #888;
  display: block;
}
.cols {
  display: flex;
}
.cols__cards {
  margin-right: 4rem;
}
.cols__filters {
  width: 37rem;
  flex-shrink: 0;
}

@media (max-width: 1000px) {
  .container {
    width: 100vw;
    padding: 4rem 2rem 8rem;
    overflow: hidden;
  }
  .cols {
    flex-wrap: wrap;
    overflow: hidden;
  }
  .cols__cards,
  .cols__filters {
    width: 100%;
    margin-left: 0;
    margin-right: 0;
  }
  .main-title {
    margin: 0 0 4rem;
    line-height: 1.3;
    font-size: 2.3rem;
  }
}
</style>
