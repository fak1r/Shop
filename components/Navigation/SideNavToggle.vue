<template>
  <div
    class="drawer-toggle"
    role="button"
    @click="$emit('toggle')"
  >
    <div class="bar" />
    <div class="bar" />
    <div class="bar" />
  </div>
</template>

<style scoped lang="scss">
  .drawer-toggle {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    height: 50%;
    width: 35px;
    cursor: pointer;
    @media (min-width: 768px) {
      display: none;
    }
  }
  
  .drawer-toggle .bar {
    width: 90%;
    height: 2px;
    background-color: white;
  }
</style>