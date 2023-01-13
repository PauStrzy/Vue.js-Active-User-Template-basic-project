<template>
	<div>
		<h2>
			Name: <span>{{ name }}</span>
		</h2>
		<h3>Age: {{ age }} Years</h3>
	</div>
</template>

<script>
export default {
	props: {
		name: { type: String, required: true },
		age: {
			type: Number,
			required: true,
		},
	},
}
</script>
