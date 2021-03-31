<template>
	<section>
		<header>
			<h1>Users</h1>
		</header>

		<div>
			<active-user :username="username" :age="age"></active-user>
			<user-data
				@update-name="updateName"
				@update-age="updateAge"
			></user-data>
		</div>
	</section>
</template>

<script>
	export default {
		data() {
			return {
				username: '',
				age: '',
			};
		},
		methods: {
			updateName(text) {
				this.username = text;
			},
			updateAge(number) {
				this.age = number;
			},
		},
	};
</script>
