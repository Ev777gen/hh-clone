<template>
  <q-header elevated class="header">
    <div class="header__toolbar_upper toolbar">
      <div class="toolbar__body container">
        <div><a href="" class="toolbar__link_dashed">Москва</a></div>
        <div class="toolbar__nav">
          <a href="" class="toolbar__link">Поиск работы</a>
          <a href="" class="toolbar__link">Продвижение резюме</a>
          <a href="" class="toolbar__link">Готовое резюме</a>
          <a href="" class="toolbar__link">Репетиция собеседования</a>
          <span>
            <a href="" class="toolbar__link_dashed">Все сервисы</a>
            <q-icon :name="fasGripVertical" class="toolbar__link-icon"/>
          </span>
        </div>
      </div>
    </div>
    <q-toolbar class="header__toolbar_lower">
      <div class="toolbar__body container">
        <div class="toolbar__nav">
          <div class="header__logo">hh</div>
          <a href="" class="toolbar__link">Мои резюме</a>
          <a href="" class="toolbar__link">Отклики</a>
          <a href="" class="toolbar__link">Помощь</a>
        </div>
        <div class="toolbar__nav">
          <span>
            <q-icon :name="fasMagnifyingGlass" class="toolbar__icon"/>
            Поиск
          </span>
          <a href="" class="toolbar__link">Создать резюме</a>
          <q-icon :name="farComment" class="toolbar__icon"/>
          <q-icon :name="farHeart" class="toolbar__icon"/>
          <q-icon :name="farBell" class="toolbar__icon"/>
          <q-icon :name="farCircleUser" class="toolbar__icon"/>
        </div>
      </div>
    </q-toolbar>
  </q-header>
</template>

<script setup lang="ts">
import {
  fasGripVertical,
  fasMagnifyingGlass,
  farComment,
  farHeart,
  farBell,
  farCircleUser,
} from '@quasar/extras/fontawesome-v6';
</script>

<style lang="scss">
.header {
  &__body {
    display: flex;
    justify-content: space-between;
  }

  // &__toolbar_upper,
  // &__toolbar_lower {
  // }
  &__toolbar_upper {
    height: 40px;
    padding-top: 10px;
    color: $blue_light;
    background-color: $background;
  }
  &__toolbar_lower {
    padding: 15px 0;
    background-color: $black;
    & .toolbar__link {
      color: white;
    }
  }

  & .toolbar {
    &__body {
      display: flex;
      justify-content: space-between;
    }

    &__nav {
      display: flex;
      align-items: center;
    }

    &__link,
    &__link_dashed {
      margin-right: 25px;
      text-decoration: none;
      color: $blue_light;
    }
    &__link_dashed {
      margin-right: 5px;
      border-bottom: 1px dashed $blue_light;
    }
    &__link-icon {
      font-size: 18px;
    }
    &__icon {
      font-size: 22px;
      font-weight: 100;
    }
  }

  &__logo {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: $red;
    line-height: 50px;
    text-align: center;
    font-size: 26px;
    font-weight: 500;
  }
}

// .icon {
//   font-size: 200px;
//   color: $blue_light;
// }
</style>
