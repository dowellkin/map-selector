<template>
  <div id="app">
		selected:
		
		<select v-model="test" name="" id="">
			<option v-for="item in data" :key="item.id" :value="item.id">{{item.id}}</option>
		</select>
		
		<div class="wrapper">
			<my-map v-model="test">

			</my-map>
		</div>
  </div>
</template>

<script>
import myMap from './components/map.vue'

export default {
  name: 'App',
  components: {
    myMap
  },
	data: () => ({
		test: "",
		data: [
			{id:"BY-BR"},{id:"BY-HO"},{id:"BY-HM"},{id:"BY-HR"},{id:"BY-MA"},{id:"BY-MI"},{id:"BY-VI"}
		]
	})
}
</script>

<style lang="sass">
#app
	font-family: Avenir, Helvetica, Arial, sans-serif
	-webkit-font-smoothing: antialiased
	-moz-osx-font-smoothing: grayscale
	text-align: center
	color: #2c3e50
	margin-top: 60px


.wrapper
	display: flex
	justify-content: center
	align-items: center
	height: 100vh

	& > *
		flex-shrink: 0
</style>
