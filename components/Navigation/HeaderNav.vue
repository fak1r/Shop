<template>
  <div class="header-container">
    <header class="the-header">
      <NavigationSideNavToggle @toggle="$emit('sidenavToggle')" />
      <div class="logo">
        <nuxt-link to="/">
          SHOP
        </nuxt-link>
      </div>
      <div class="spacer" />
      <div class="navigation-items">
        <ul class="nav-list">
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
    </header>
  </div>
</template>
  
<style scoped lang="scss">
.header-container {
  height: 60px;
}

.the-header {
  width: 100%;
  position: fixed;
  height: 60px;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: black;
  z-index: 100;
  box-sizing: border-box;
  padding: 0 20px;
}

.logo {
  margin: 0 10px;
  font-size: 1.3rem;
}

.logo a {
  text-decoration: none;
  color: white;
}

.navigation-items {
  display: none;
}
 
@media (min-width: 768px) {
  .navigation-items {
    display: block;
  }
}

.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

.nav-item {
  margin: 0 10px;
}

.nav-item a {
  text-decoration: none;
  color: white;
}

.spacer {
  flex: 1;
}

.nav-item a {
  &:hover, &:active, &.router-link-exact-active {
    color: green;
  }
}

  
</style>