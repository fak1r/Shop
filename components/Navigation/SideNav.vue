<template>
  <div class="sidenav-container">
    <div
      v-if="show"
      class="sidenav-backdrop"
      @click="$emit('close')"
    />
    <transition name="slide-side">
      <div
        v-if="show"
        class="sidenav"
      >
        <ul
          class="nav-list"
          @click="$emit('close')"
        >
          <li class="nav-item">
            <nuxt-link to="/">
              Main page
            </nuxt-link>
          </li>
          <li class="nav-item">
            <nuxt-link to="/products">
              Products
            </nuxt-link>
          </li>
        </ul>
      </div>
    </transition>
  </div>
</template>

<script setup lang="ts">
  
  defineProps({
    show: {
      type: Boolean,
      default: false
    }
  })
  
  defineEmits(['close']);

</script>

<style scoped>
.sidenav-container {
  height: 100%;
  width: 100%;
}

.sidenav-backdrop {
  height: 100%;
  width: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 1000;
  position: fixed;
  top: 0;
  left: 0;
}

.sidenav {
  height: 100%;
  width: 300px;
  background-color: white;
  z-index: 10000;
  position: fixed;
  top: 0;
  left: 0;
  box-sizing: border-box;
  padding: 30px;
}

.slide-side-enter-active, .slide-side-leave-active {
  transition: all .3s ease-out;
}

.slide-side-enter-from, .slide-side-leave-to {
  transform: translateX(-100%);
}

.slide-side-enter-to {
  transform: translateX(100%, 0);
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
  width: fit-content;
}

.nav-item {
  margin: 20px 0;
}

.nav-item a {
  text-decoration: none;
  color: black;
}
</style>