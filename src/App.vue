<template>
  <div class="container">
    <div>
      <Header :MenuVisible="MenuVisible" :Portrait="Portrait" @toggle-menu="toggleMenu" />
    </div> 
    <div class="profile">
      <AppMenu :MenuVisible="MenuVisible" />
      <Profile />
    </div>  
  </div>
  
</template>

<script>
import Header from './components/Header.vue';
import AppMenu from './components/App_menu.vue';
import Profile from './components/Profile.vue';

export default {
  components: {
    Header,
    AppMenu,
    Profile
  },
  data() {
    return {
      MenuVisible: false,
      Portrait: false 
    };
  },
  methods: {
    toggleMenu() {
      this.MenuVisible = !this.MenuVisible;
    },
    handleOrientationChange() {
      this.Portrait = window.innerHeight > window.innerWidth;
      this.MenuVisible = !this.Portrait;
    }
  },
  mounted() {
    window.addEventListener('resize', this.handleOrientationChange);
    this.handleOrientationChange();
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.handleOrientationChange);
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/styles/admin_panel.scss';
</style>
