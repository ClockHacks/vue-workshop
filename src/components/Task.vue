<template>
	<div id="task" :class="done ? 'done' : ''">
		<input type="checkbox" v-model="done">
		{{ text }}!!
	</div>
</template>

<script>
export default {
	data() {
		return {
			// textVar: "some placeholder text",
			done: false
		}
	},
	props: {
		text: String
	}
}
</script>

<style>
#task {
	border: 1px;
	background-color: white;
	padding: 10px;
	border-radius: 5px;
	color: black;
	margin: 5px;
}

.done {
	text-decoration: line-through;
	opacity: 0.5;
}
</style>
