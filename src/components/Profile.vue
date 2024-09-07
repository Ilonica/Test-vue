<template>
  <div class="profile">
    <div class="app-panel">
      <div class="title">
        <img src="@/assets/image/User_ic.svg" />
        <p class="text-buttons ibm-plex-sans-regular-500">Профиль</p>
      </div>
      <button class="icon-button-app">
        <img src="@/assets/image/Flash_ic.svg" />
      </button>
    </div>
    <div class="block-panel">
      <div class="fio">
        <img src="@/assets/image/User_FIO_ic.svg" />
        <p class="text-fio ibm-plex-sans-regular-400">ФИО</p>
      </div>
      <button class="icon-button-block" @click="toggleEdit">
        <img src="@/assets/image/Edit_ic.svg" />
      </button>
    </div>
    <div class="block-content">
      <div class="fio-edit" v-for="(field, index) in fields" :key="index">
        <p class="text-fio-edit ibm-plex-sans-regular-400">{{ field.label }}</p>
        <input 
          v-if="isEditing"
          class="edit-fio ibm-plex-sans-regular-400"
          :placeholder="field.value"
        />
        <p v-else class="text-fio-data ibm-plex-sans-regular-400">Не указано</p>
      </div>
    </div>
  </div>
  </template>
  
  <script>
  export default {
    name: 'ProfilE',
    data() {
    return {
      isEditing: false,
      fields: [
        { label: 'Фамилия', value: 'Иванов' },
        { label: 'Имя', value: 'Иван' },
        { label: 'Отчество', value: 'Иванович' },
      ],
    };
  },
  methods: {
    toggleEdit() {
      this.isEditing = !this.isEditing;
    },
  },
};
  </script>
  
  <style lang="scss" scoped>
  @import '@/assets/styles/profile.scss';
  </style>
  