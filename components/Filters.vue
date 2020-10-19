<template>
  <div class="filters" :class="{ show: show }">
    <button class="filters__close-btn" @click="show = false">закрыть</button>
    <button class="filters__open-btn" @click="show = true">Открыть</button>
    <h4 class="filters__title">Фильтры</h4>
    <form action="" class="filters__form">
      <div class="filters__group">
        <h5 class="filters__group-title">Пол</h5>
        <div class="filters__group-inline">
          <label class="filters__label">
            <input
              name="sex"
              value="male"
              type="radio"
              class="filters__label-input"
            />
            <i class="filters__label-marker"></i>
            Мужской
          </label>
          <label class="filters__label">
            <input
              name="sex"
              value="female"
              type="radio"
              class="filters__label-input"
            />
            <i class="filters__label-marker"></i>
            Женский
          </label>
        </div>
      </div>
      <div class="filters__group">
        <h5 class="filters__group-title">Акция</h5>
        <div class="filters__group-item">
          <label class="filters__label">
            <input
              name="dependencies"
              type="checkbox"
              class="filters__label-input"
            />
            <i class="filters__label-marker"></i>
            30 минут бесплатно
          </label>
        </div>
      </div>
      <div class="filters__group">
        <h5 class="filters__group-title">Вопросы психологу</h5>
        <div class="filters__group-list">
          <div class="filters__group-subtitle">Зависимости</div>
          <div class="filters__group-item">
            <label class="filters__label">
              <input
                name="dependencies"
                type="checkbox"
                class="filters__label-input"
              />
              <i class="filters__label-marker"></i>
              Психологическая зависимость
            </label>
          </div>
          <div class="filters__group-item">
            <label class="filters__label">
              <input
                name="dependencies"
                type="checkbox"
                class="filters__label-input"
              />
              <i class="filters__label-marker"></i>
              Зависимые отношения
            </label>
          </div>
          <div class="filters__group-item">
            <label class="filters__label">
              <input
                name="dependencies"
                type="checkbox"
                class="filters__label-input"
              />
              <i class="filters__label-marker"></i>
              Игровая зависимость
            </label>
          </div>
          <div class="filters__group-item">
            <label class="filters__label">
              <input
                name="dependencies"
                type="checkbox"
                class="filters__label-input"
              />
              <i class="filters__label-marker"></i>
              Алкогольная зависимость
            </label>
          </div>
        </div>
      </div>
      <div class="filters__actions">
        <button class="filters__btn">Применить</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Filters',
  data() {
    return {
      show: true,
    }
  },
}
</script>

<style lang="scss" scoped>
.filters {
  box-sizing: border-box;
  padding: 3.5rem 3rem;
  background: #fff;
  border-radius: 0.3rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.08);
}
.filters__title {
  line-height: 1.4;
  font-size: 1.8rem;
  margin-top: 0;
  margin-bottom: 2.2rem;
  color: #455a64;
}
.filters__group {
  margin: 0 0 2.5rem;
}
.filters__group-title {
  padding: 0.1rem 0 0 0.1rem;
  font-size: 1.4rem;
  font-weight: 700;
  color: #78909c;
  margin-bottom: 1.5rem;
}
.filters__group-subtitle {
  font-size: 1.1rem;
  line-height: 2;
  margin: 2rem 0 0;
  text-transform: uppercase;
  letter-spacing: 0.05rem;
}
.filters__label-input {
  display: none;
}
.filters__label {
  display: flex;
  position: relative;
  padding-left: 3rem;
  margin-right: 2rem;
  font-size: 1.3rem;
  font-weight: 400;
  height: 1.9rem;
  line-height: 1.95rem;
  color: #78909c;
  cursor: pointer;
}
.filters__label-marker {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  height: 2rem;
  width: 2rem;
  background-position: center;
  background-repeat: no-repeat;
  cursor: pointer;
  background-color: #fff;
  border: 0.1rem solid #bcbcba;
  box-sizing: border-box;
}
input[type='radio'] ~ .filters__label-marker {
  border-radius: 50%;
}
input[type='checkbox'] ~ .filters__label-marker {
  border-radius: 0.4rem;
}
input:checked ~ .filters__label-marker {
  border: 0.1rem solid #24c0a7;
  background: #24c0a7;
}
input[type='radio']:checked ~ .filters__label-marker {
  background-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiI+PGNpcmNsZSBmaWxsPSIjRkZGIiBjeD0iOCIgY3k9IjgiIHI9IjgiLz48L3N2Zz4=);
  background-repeat: no-repeat;
  background-size: 0.8rem;
  background-position: center;
}
input[type='checkbox']:checked ~ .filters__label-marker {
  background-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgaGVpZ2h0PSIxNiI+PHBhdGggZmlsbD0iI0ZGRiIgZD0iTTEzLjMzOC40NjNhMS40NzQgMS40NzQgMCAwIDEgMS4xNS0uNDYxYy4zODEuMDE1Ljc0NC4xOTIgMS4wMDYuNDY0LjMyNC4zMDYuNTE4Ljc0OC41MDUgMS4xOTIgMCAuMzIzLS4xMTQuNjM4LS4zMDIuOTAxLTIuNzA5IDMuODU3LTUuNDIyIDcuNzE0LTguMTMgMTEuNTcxLS4yODMuNDAxLS43Mi42ODgtMS4xOTguODA2LS4yOTguMDc4LS42MDguMDYzLS45MTIuMDYzYTEuMjg4IDEuMjg4IDAgMCAxLTEtLjUyN2MtMS4zMzItMS44NC0yLjY2My0zLjY3OC0zLjk5Ni01LjUxNS0uMDk1LS4xMzQtLjE5Ny0uMjY0LS4yNzgtLjQwNy0uMS0uMTctLjE0OS0uMzY0LS4xODMtLjU1N3YtLjIyN2MuMDM4LS40OC4zMTctLjkzMy43NDItMS4xNzRhMS42NSAxLjY1IDAgMCAxIDEuNDY0LS4xMDFjLjI0My4xMDEuNDU2LjI2Mi42MjUuNDYuNjQ1Ljc0MiAxLjI5MiAxLjQ4NSAxLjkzNyAyLjIyOWEuMzgyLjM4MiAwIDAgMCAuMjI1LjE0Yy4xNjktLjAyMS4yNjQtLjE3OC4zNzQtLjI5MUM4LjAyNCA2LjE3NSAxMC42OCAzLjMxNyAxMy4zMzguNDYzeiIvPjwvc3ZnPg==);
  background-repeat: no-repeat;
  background-size: 1rem;
  background-position: center;
}

.filters__group-inline {
  display: flex;
}

.filters__group-item {
  margin: 1.5rem 0 0.4rem;
}
.filters__btn {
  background: #24c0a7;
  color: #fff;
  transition: background 0.2s linear;
  border-radius: 0.3rem;
  text-transform: uppercase;
  font-weight: 700;
  line-height: 3.4rem;
  height: 3.4rem;
  border: none;
  box-shadow: none;
  padding: 0 1.2rem;
  cursor: pointer;
  &:hover {
    background-color: #009688;
  }
}

.filters > .filters__open-btn,
.filters > .filters__close-btn {
  display: none;
}

@media (max-width: 1000px) {
  .filters {
    height: 5rem;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 0;
    &.show {
      padding: 6.5rem 3rem 3.5rem;
      top: 0;
      width: 100vw;
      min-height: 100vh;
      display: block;
    }
  }
  .filters > .filters__open-btn {
    height: 5rem;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    width: 100%;
    border: none;
    text-indent: -9999px;
    background-color: #fff;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='i-round-tune' viewBox='0 0 24 24'%3E%3Cpath d='M3 18c0 .55.45 1 1 1h5v-2H4c-.55 0-1 .45-1 1zM3 6c0 .55.45 1 1 1h9V5H4c-.55 0-1 .45-1 1zm10 14v-1h7c.55 0 1-.45 1-1s-.45-1-1-1h-7v-1c0-.55-.45-1-1-1s-1 .45-1 1v4c0 .55.45 1 1 1s1-.45 1-1zM7 10v1H4c-.55 0-1 .45-1 1s.45 1 1 1h3v1c0 .55.45 1 1 1s1-.45 1-1v-4c0-.55-.45-1-1-1s-1 .45-1 1zm14 2c0-.55-.45-1-1-1h-9v2h9c.55 0 1-.45 1-1zm-5-3c.55 0 1-.45 1-1V7h3c.55 0 1-.45 1-1s-.45-1-1-1h-3V4c0-.55-.45-1-1-1s-1 .45-1 1v4c0 .55.45 1 1 1z'%3E%3C/path%3E%3C/svg%3E");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 18px;
    box-shadow: 0 0 2rem rgba(0, 0, 0, 0.19),
      0 0.6rem 0.6rem rgba(0, 0, 0, 0.23);
  }
  .filters > .filters__close-btn {
    display: none;
    position: absolute;
    right: 3rem;
    top: 3rem;
    background-color: #fff;
    border: none;
    height: 2rem;
    width: 2rem;
    text-indent: -9999px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' id='i-round-close' viewBox='0 0 24 24'%3E%3Cpath d='M18.3 5.71c-.39-.39-1.02-.39-1.41 0L12 10.59 7.11 5.7c-.39-.39-1.02-.39-1.41 0-.39.39-.39 1.02 0 1.41L10.59 12 5.7 16.89c-.39.39-.39 1.02 0 1.41.39.39 1.02.39 1.41 0L12 13.41l4.89 4.89c.39.39 1.02.39 1.41 0 .39-.39.39-1.02 0-1.41L13.41 12l4.89-4.89c.38-.38.38-1.02 0-1.4z'%3E%3C/path%3E%3C/svg%3E");
  }
  .filters.show > .filters__close-btn {
    display: block;
  }
  .filters.show > .filters__open-btn {
    display: none;
  }
}
</style>
