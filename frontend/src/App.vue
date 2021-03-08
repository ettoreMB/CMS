<template>
	<div id="app" :class="{'hide-menu' :!isMenuVisible}">
		<Header 
			title="CMS-COD3R" 
			:hideToggle="true"
			:hideUserDrodown="true"
		/>
		<Menu />
		<Content />
		<Footer />
	</div>
</template>

<script>
import {mapState} from 'vuex'
import Header from './components/template/Header'
import Content from './components/template/Content'
import Menu from './components/template/Menu'
import Footer from "./components/template/Footer"

export default {
	name: "App",
	components: {Header, Content, Menu, Footer},
	computed: mapState(['isMenuVisible']),
 }
</script>

<style>
	* {
		margin: 0;
		padding: 0;

		font-family: "Lato", sans-serif;
	}

	#app {
			--webkit-font-smoothing: antialiased;
			--moz-osx-font-smoothing: grayscale;

			height: 100vh;
			display: grid;
			grid-template-rows: 60px 1fr 40px;
			grid-template-columns: 300px 1fr;
			grid-template-areas: 
			"header header"
			"menu content"
			"menu footer";
		}

		#app.hide-menu {
			grid-template-areas: 
				"header header"
				"content content"
				"footer footer";
		}
</style>