<template>
	<h1>Current Number {{ numero }}</h1>

	<button @click="lessMore">Less</button>
	<button @click="addMore">Add</button>

	<div class="container">
		<p v-if="numero >= 10">Es mayor o igual que 10</p>

		<p v-else-if="numero > 0 && numero < 10">
			mayor que 0 pero merno que 10
		</p>

		<p v-else>es menor que 0</p>
	</div>
</template>

<script>
export default {
	name: "HelloWorld",
	props: {
		msg: String,
	},
	data() {
		return {
			numero: -1,
		};
	},
	methods: {
		addMore() {
			this.numero += 1;
		},
		lessMore() {
			this.numero -= 1;
		},
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
	margin: 40px 0 0;
}
ul {
	list-style-type: none;
	padding: 0;
}
li {
	display: inline-block;
	margin: 0 10px;
}
a {
	color: #42b983;
}
</style>
