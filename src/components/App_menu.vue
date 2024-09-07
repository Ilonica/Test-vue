<template>
  <div v-if="MenuVisible" class="menu">
    <button class="icon-buttons-active ibm-plex-sans-regular"> 
        <img src="@/assets/image/User_ic.svg">
        <p class="text-buttons">Профиль</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Document_ic.svg">
        <p class="text-buttons">Документы</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Phone_ic.svg">
        <p class="text-buttons">Контактные данные</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Lock_Close_ic.svg">
        <p class="text-buttons">Доступ</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Sessions_ic.svg">
        <p class="text-buttons">Сессии</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Users_group_ic.svg">
        <p class="text-buttons">Группы</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Location_ic.svg">
        <p class="text-buttons">Часовой пояс</p>
    </button>
    <button class="icon-buttons ibm-plex-sans-regular"> 
        <img src="@/assets/image/Apps_atalog_ic.svg">
        <p class="text-buttons">Приложения</p>
    </button>
  </div>
</template>

<script>
export default {
  name: 'AppMenu',
  props: {
    MenuVisible: {
      type: Boolean,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/app_menu.scss';
</style>
