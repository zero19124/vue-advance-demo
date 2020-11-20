<template>
	<div>

		<h2>{{header}}</h2>

		<input type="text" class="form-control" v-model="val"
		ref="input" @input="changeInput"/>

	</div>
</template>

<script>
	export default {
		data() {
			return {
				header:"标题",
				val: '输入框'
			}
		},
		methods: {
			focus() {
				this.$refs.input.focus()
			},
			renameHeader(data){
				this.header = data
			},
			changeInput(e){
				this.$parent.header = e.target.value
				this.$parent.parentRename(e.target.value)
			}
		},
	}
</script>

<style>
</style>
