<template>
  <q-header elevated>
    <div class="toolbar">
      <div class="toolbar__body container">
        <div>
          <a href="" class="toolbar__location">Москва</a>
          <span v-if="!isAuthUser" class="toolbar__current-tub">Соискателям</span>
          <a href="" v-if="!isAuthUser" class="toolbar__link">Работодателям</a>
        </div>
        <div class="toolbar__links">
          <a href="" v-if="isAuthUser" class="toolbar__link">Поиск работы</a>
          <a href="" v-if="isAuthUser" class="toolbar__link">Продвижение резюме</a>
          <a href="" class="toolbar__link">Готовое резюме</a>
          <a href="" class="toolbar__link">Репетиция собеседования</a>
          <span>
            <a href="" class="toolbar__link_dashed">Все сервисы</a>
            <q-icon :name="fasGripVertical" class="toolbar__icon"/>
          </span>
        </div>
      </div>
    </div>
    <q-toolbar class="navbar">
      <div class="navbar__body container">
        <div class="navbar__links">
          <div class="navbar__logo">hh</div>
          <a href="" v-if="isAuthUser" class="navbar__link">Мои резюме</a>
          <a href="" v-if="isAuthUser" class="navbar__link">Отклики</a>
          <a href="" class="navbar__link_dashed">Помощь</a>
        </div>
        <div class="navbar__links">
          <a href="" class="navbar__link">
            <q-icon :name="fasMagnifyingGlass" class="navbar__icon"/>
            Поиск
          </a>
          <a href="" class="navbar__button">Создать резюме</a>
          <a href=""  v-if="!isAuthUser" class="navbar__button_white">Войти</a>
          <span v-if="isAuthUser">
            <q-icon :name="farComment" class="navbar__icon"/>
            <q-icon :name="farHeart" class="navbar__icon"/>
            <q-icon :name="farBell" class="navbar__icon"/>
            <q-icon :name="farCircleUser" class="navbar__icon"/>
          </span>
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
import { ref } from 'vue';

const isAuthUser = ref(true);
</script>

<style lang="scss">
.toolbar {
  height: 40px;
  padding-top: 10px;
  color: $blue_light;
  background-color: $background;

  &__body {
    display: flex;
    justify-content: space-between;
  }

  &__links {
    display: flex;
    align-items: center;
  }
  &__location,
  &__link,
  &__link_dashed {
    margin-right: 25px;
    text-decoration: none;
    color: $blue_light;
  }
  &__location {
    margin-right: 40px;
    border-bottom: 1px dashed $blue_light;
  }
  &__link_dashed {
    margin-right: 5px;
    border-bottom: 1px dashed $blue_light;
  }
  &__current-tub {
    margin-right: 25px;
    color: $black;
  }

  &__icon {
    font-size: 18px;
  }
}

.navbar {
  padding: 15px 0;
  background-color: $black;
  & .toolbar__link {
    color: white;
  }

  &__body {
    display: flex;
    justify-content: space-between;
  }

  &__logo {
    width: 50px;
    height: 50px;
    margin-right: 10px;
    border-radius: 50%;
    line-height: 50px;
    text-align: center;
    font-size: 26px;
    font-weight: 500;
    background-color: $red;
  }

  &__links {
    display: flex;
    align-items: center;
  }

  &__link,
  &__link_dashed {
    margin-left: 20px;
    font-size: 16px;
    color: white;
    text-decoration: none;
  }

  &__link_dashed {
    border-bottom: 1px dashed white;
  }

  &__button,
  &__button_white {
    margin-left: 28px;
    margin-right: 0px;
    padding: 10px 15px;
    border: 1px solid $green_light_dull;
    border-radius: 30px;
    font-size: 16px;
    color: $green-light;
    text-decoration: none;
    &:hover {
      border: 1px solid $green-light;
    }
  }
  &__button_white {
    border: 1px solid #999;
    color: white;
    &:hover {
      border: 1px solid white;
    }
  }

  &__icon {
    margin-left: 28px;
    font-size: 22px;
    font-weight: 100;
    color: white;
  }
}
</style>
