<template>
	<div style="width: 100px;margin: auto;">

		<!-- 获取普通元素 -->
		<!-- <input type="text" class="form-control" ref="input"/> -->
		<!-- 获取列表 -->
		<!-- <ul class="list-group">
			<li class="list-group-item" v-for="(item,index) in list" :key="index"
			ref="list">
				{{item}}
			</li>
		</ul> -->

   <!-- <ul>
      <li ref="list" class="list-group-item" v-for="(item,index) in list" :key="index">{{item}}</li>
    </ul> -->


		<!-- 获取组件 -->
		<demo-item ref="demoitem"></demo-item>

		<!-- $children -->
		<!-- <h1>11</h1> -->
		<demo-item></demo-item>
		<!-- <demo-item></demo-item> -->
		<!-- <demo-item></demo-item> -->

		<!-- $parent -->
		<!-- <h1 class="text-center">{{header}}</h1>
		<demo-item></demo-item> -->

	</div>
</template>

<script>
import demoItem from './demo-item.vue';
	export default {

    components: {
      demoItem
    },
		data() {
			return {
				header:"我是父组件",
				list: [1,2,3,4,5,6,7,8,9,10]
			}
		},
		// 页面渲染完成
		mounted() {
			// 获取input
			// console.log(this.$refs.input)

			// 修改样式
			// this.$refs.input.style.borderColor = 'red'

			// 获取焦点
			// this.$refs.input.focus()


			// 获取列表
			// console.log(this.$refs.list);


			// 加随机颜色
			// this.$refs.list.forEach( v =>{
   //      v.style.backgroundColor = '#'+Math.floor(Math.random()*1000000)
   //    })

			// 获取$refs子组件
			// console.log(this.$refs)

			// 操作子组件方法
			// console.log('父组件操作子组件')
			// this.$refs.demoitem.focus()

			// this.$refs.demoitem.renameHeader(32)
//
			// this.$refs.demoitem.val = '父组件修改子组件'


			console.log(this.$children)
			this.$children[1].val = '修改第一个'

		},
		methods: {
			parentRename(data) {
				this.header = data
			}
		},
	}
</script>

<style>
</style>
