<template>
	<div>
		<h1>登录</h1>
		<ul>
			<li>
				<label for="">用户名</label>
				<input type="text" v-model="username" id="name" />
			</li>
			<li>
				<label for="">密码</label>
				<input type="text" v-model="password" id="pw" />
			</li>
			<li><input type="button" value="提交" @click="login" /></li>
		</ul>
	</div>
</template>

<script>
	import { LoginServlet } from '../../api/api.js'
	export default {
		data() {
			return {
				username: "",
				password: ""
			}
		},
		methods: {
			login: function() {
				//调用登录接口
				LoginServlet({
					userName: this.username,
					passWord: this.password
				}).then(function(response) {
					if(response.meta.status === 200){
						// 跳转路由
						this.$router.push({name:'home'});
					}else {
						console.log("")
					}
					 
				})

			}
		}
	}
</script>

<style scoped>

</style>