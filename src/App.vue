<template>
  <div id="app">
    <h1>Vue Google Serp simulator</h1>
    <vue-google-serp
      title="Titles are truncated when they exceed the 60 characters limit."
      url="https://www.example.com"
      description="Example Domain. This domain is established to be used for illustrative examples in documents. You may use this domain in examples without prior coordination or asking for permission. – Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras rutrum sed eros iaculis congue."
    />
  </div>
</template>

<script>
import vueGoogleSerp from "./components/vueGoogleSerp.vue"

export default {
	name: "app",
	components: {
		vueGoogleSerp
	}
}
</script>

<style lang="scss">
#app {
  font-family: arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
  padding: 25px;
}
</style>
