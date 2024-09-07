<template>
 <div class="header">
    <div class="company">
      <p>Тест</p>
      <button class="icon-menu" v-if="Portrait" @click="$emit('toggle-menu')">
        <img class="icon" src="@/assets/image/free-icon-menu-2976215.png" v-if="!MenuVisible"/>
        <img class="icon" src="@/assets/image/free-icon-arrow-10412365.png" v-if="MenuVisible"/>
      </button>
    </div>
    <div class="person ibm-plex-sans-regular">
      <p class="name">Константинопольский Константин Константинович</p>
      <div class="action-buttons">
        <button class="icon-buttons"><img src="@/assets/image/Open_panel_left_ic.svg"></button>
        <button class="icon-buttons"><img src="@/assets/image/Application_ic.svg"></button>
        <button class="icon-buttons"><img src="@/assets/image/Palitre.svg"></button>
        <div class="avatar"><img class="avatar-image" src="@/assets/image/avatar.png"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeadeR',
  props: {
    MenuVisible: {
      type: Boolean,
      required: true
    },
    Portrait: { 
      type: Boolean,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/header.scss';
</style>


