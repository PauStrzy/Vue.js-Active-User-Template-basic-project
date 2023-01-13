<template>
	<section>
		<header>
			<h1>Active User</h1>
		</header>
		<div>
			<active-user :name="name" :age="age"></active-user>
			<user-data @add-user="addUser"></user-data>
		</div>
	</section>
</template>

<script>
export default {
	data() {
		return {
			name: 'Paulina',
			age: '28',
		}
	},

	methods: {
		addUser(name, age) {
			this.name = name
			this.age = +age
		},
	},
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');

* {
	box-sizing: border-box;
}

html {
	font-family: 'Jost', sans-serif;
}

body {
	margin: 0;
}
section {
	margin: 3rem auto;
	padding: 1rem;
	border: 1px solid #2b4d384b;
	border-radius: 8px;
	text-align: center;
	width: 90vw;
	color: #2b4d38;
	font-size: 2rem;
	max-width: 40rem;
}

header {
	box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
	border-radius: 8px;
	padding: 0.1rem 0;
	background-color: #437858;
	color: #fff;
	text-align: center;
	max-width: 40rem;
}

#app div h2,
h3 {
	font-size: 3rem;
	margin: 0.5em;
}

#app span {
	text-transform: uppercase;
}
#app div {
	padding: 1rem;
	max-width: 40rem;
	background-color: rgb(243, 241, 241);
	border: 1px dashed #2b4d382a;
	border-radius: 8px;
}
/* #app label {
	display: block;
	margin: 0.5rem;
	width: 40%;
} */
#app div input {
	padding: 0.3em;
	margin: 0.4em;
	text-align: center;
	font: inherit;
	font-size: 1.5rem;
}
button {
	padding: 0.05rem 1rem;
	margin: 1em auto;
	height: 2em;
	width: 20rem;
	font-size: 2rem;
	border-radius: 8px;
	font: inherit;
	cursor: pointer;
	background-color: #fff;
	color: #437858;
	box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
	transition: 0.3s;
}

#app button:hover,
#app button:active {
	background-color: #4d9168;
	border-color: #437858;
	color: #fff;
	box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
}
</style>
