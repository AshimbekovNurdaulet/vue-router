<template>
  <div id="app">
    <div id="nav">
<!--      <router-link to="/">Home</router-link> |-->
<!--      <router-link to="/example">Example</router-link>-->

      <header>
        <div class="navbar">
          <div class="container">
            <div class="navbar-content">
              <div class="logo">VUE-CLI</div>
              <ul class="navbar-list">
                <li class="navbar-item" v-for="link in links" :key="link.title">
                    <router-link class="navbar-link" :title="link.title" :to="link.url">{{ link.title }}</router-link>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </header>
    </div>
<!--    <router-view/>-->

  <router-view></router-view>

  </div>
</template>


<script>
export default {
  data() {
    return {
      links: [
        { title: 'Home', url: '/'},
        { title: 'Example', url: '/example'},
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
