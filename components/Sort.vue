<template>
  <div class="sort">
    <span class="sort__title">Сортировка</span>
    <ul class="sort__list">
      <li class="sort__item">
        <a href="#" class="sort__link">Консультации</a>
      </li>
      <li class="sort__item"><a href="#" class="sort__link">Стоимость</a></li>
      <li class="sort__item"><a href="#" class="sort__link">Отзывы</a></li>
      <li class="sort__item"><a href="#" class="sort__link">Стаж</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Sort',
}
</script>

<style scoped>
.sort {
  margin: 0 0 3rem;
  position: relative;
  white-space: nowrap;
  display: flex;
  align-items: center;
}
.sort__title {
  padding-right: 2rem;
  color: #90a4ae;
}
.sort__list {
  list-style: none;
  padding: 0;
  max-width: 138rem;
  display: flex;
  overflow: hidden;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  -webkit-tap-highlight-color: transparent;
  -ms-overflow-style: -ms-autohiding-scrollbar;
  flex-grow: 0;
}
.sort__item {
  display: flex;
  align-items: center;
  padding: 1rem 1.5rem;
  font-size: 1.5rem;
  font-weight: 700;
  color: #37474f;
  cursor: pointer;
}
.sort__link {
  color: #0fc1a7;
  text-decoration: none;
}
@media (max-width: 1000px) {
  .sort {
    background-color: #fff;
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.08);
  }
  .sort__title {
    display: none;
  }
  .sort__item {
    padding: 1.5rem 1.5rem 1.7rem 2rem;
    font-size: 1.5rem;
  }
}
</style>
