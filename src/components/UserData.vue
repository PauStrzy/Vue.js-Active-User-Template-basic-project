<template>
	<div class="new-user">
		<form @submit.prevent="submitData">
			<!-- <label>New Name</label> -->
			<input type="text" v-model="enteredName" placeholder="New name" />

			<!-- <label>New Age</label> -->
			<input type="text" v-model="enteredAge" placeholder="New age" />
			<button>Set User</button>
		</form>
	</div>
</template>

<script>
export default {
	emits: ['add-user'],
	data() {
		return {
			enteredName: '',
			enteredAge: '',
		}
	},
	methods: {
		submitData() {
			this.$emit('add-user', this.enteredName, this.enteredAge)
		},
	},
}
</script>
