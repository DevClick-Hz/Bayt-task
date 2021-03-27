<template>
  <div id="app">
    <div id="nav">
      <div class="tabs">
        <h4 class="logo"><i class="fas fa-home"></i> Logo</h4>
        <div :class="openMenu ? 'open' : 'links'">
          <router-link to="/">Team</router-link>
          <router-link to="/">Work</router-link>
          <router-link to="/">Price</router-link>
          <router-link to="/">Contact</router-link>
          <div class="dropdown">
            <button class="dropbtn">
              Dropdown
              <i class="fa fa-caret-down"></i>
            </button>
            <div class="dropdown-content">
              <a href="#">dumy text</a>
              <a href="#">dumy text</a>
              <a href="#">dumy text</a>
            </div>
          </div>
        </div>
      </div>
      <div class="search">
        <h4><i class="fas fa-search"></i></h4>
      </div>
      <div class="ham" @click="opened">
        <h4><i class="fas fa-bars"></i></h4>
      </div>
    </div>
    <router-view />
    <div class="foot">
      <i class="fas fa-chevron-circle-up" @click="toTop"></i>
      <p>follow us</p>
      <i class="fab fa-facebook-f"></i>
      <i class="fab fa-twitter"></i>
      <i class="fab fa-google-plus-g"></i>
      <i class="fab fa-instagram"></i>
      <i class="fab fa-linkedin-in"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      openMenu: false,
    };
  },
  methods: {
    opened() {
      this.openMenu = !this.openMenu;
    },
    toTop() {
      document.body.scrollTop = 0;
      document.documentElement.scrollTop = 0;
    },
  },
};
</script>
<style>
html,
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
h4 {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  background-color: black;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #ffffff;
  padding: 0 1rem 0 0;
  position: relative;
}

#nav a {
  color: #ffffff;
  margin: 0 0.5rem;
  padding: 0.7rem;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #ffffff;
}
.tabs,
.links {
  display: flex;
  align-items: center;
}
.logo {
  background-color: rgb(0, 119, 119);
  padding: 0.7rem 1rem;
}
.ham {
  display: none;
}
.dropdown {
  float: left;
  overflow: hidden;
}

.dropdown .dropbtn {
  font-size: 16px;
  border: none;
  outline: none;
  color: white;
  background-color: inherit;
  font-family: inherit;
  margin: 0;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #000000;
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
  padding: 0.5rem 0;
}

.dropdown-content a {
  float: none;
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
  text-align: left;
}
.dropdown:hover .dropdown-content {
  display: block;
}
.search {
  cursor: pointer;
}
.foot {
  background-color: black;
  color: white;
  padding: 3rem 0;
  position: relative;
}
.foot .fab {
  padding: 0.7rem 0.5rem;
  background-color: rgb(0, 119, 119);
  width: 25px;
  margin: 0 0.3rem;
  cursor: pointer;
}
.foot p {
  font-size: 1.2rem;
}
.foot .fas {
  position: absolute;
  right: 1rem;
  top: -20px;
  padding: 1rem;
  background-color: black;
  cursor: pointer;
}
/* ------- media query -------*/
@media screen and (max-width: 600px) {
  .search,
  .dropbtn,
  .links {
    display: none;
  }
  .open {
    position: absolute;
    display: flex;
    flex-direction: column;
    width: 100%;
    background-color: black;
    padding: 1rem 0;
    top: 40.3px;
  }
  .ham {
    display: block;
    cursor: pointer;
  }
}
</style>
