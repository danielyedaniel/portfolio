<template>
  <nav>
    <a v-for="section in sections" v-bind:key="section.name" v-bind:href="section.url" v-on:click="navigateTo(section)" class="nav-link">{{ section.name }}</a>
  </nav>
</template>

<style>
.Navigator {
  display: flex;
  align-items: center;
  background: linear-gradient(to right, #4c669f, #3b5998);
  color: white;
  font-family: 'Roboto', sans-serif;
}

.nav-link {
  display: inline-block;
  border-radius: 4px;
  padding: 8px;
  margin: 8px;
  text-decoration: none;
  transition: all 0.2s ease-in-out;
}

.nav-link:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: scale(1.1);
}

.nav-link:active {
  background-color: rgba(255, 255, 255, 0.2);
}
</style>

<script>
export default {
  data() {
    return {
      sections: [
        { name: 'Home', url: '/home' },
        { name: 'About', url: '/about' },
        { name: 'Contact', url: '/contact' }
      ]
    }
  },
  methods: {
    navigateTo(section) {
      this.$router.push(section.url)
    }
  }
}
</script>
