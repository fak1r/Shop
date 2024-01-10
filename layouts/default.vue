<template>
  <div>
    <HeaderNav @sidenav-toggle="displaySidenav = !displaySidenav" />
    <SideNav
      :show="displaySidenav"
      @close="displaySidenav = false"
    />
    <slot />
  </div>
</template>

<script setup>

  import HeaderNav from '~/components/Navigation/HeaderNav.vue';
  import SideNav from '~/components/Navigation/SideNav.vue';

  const displaySidenav = ref(false);

</script>