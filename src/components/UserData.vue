<template>
	<div>
		<input
			type="text"
			placeholder="type the name"
			v-model="username"
			@input="changeUsername"
		/>
		<input
			type="number"
			placeholder="type the age"
			v-model="age"
			@input="changeAge"
		/>
	</div>
</template>

<script>
	export default {
		emits: ['update-name', 'update-age'],
		data() {
			return {
				username: '',
				age: '',
			};
		},
		methods: {
			changeUsername(event) {
				this.$emit('update-name', event.target.value);
			},
			changeAge(event) {
				this.$emit('update-age', event.target.value);
			},
		},
	};
</script>
