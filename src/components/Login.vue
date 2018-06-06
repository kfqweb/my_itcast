<template>
	<div>
		<!--<h1>登录</h1>
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
		</ul>-->
		<header class="mui-bar mui-bar-nav">
			<h1 class="mui-title">登录</h1>
		</header>
		<div class="bsody">
			<!--<img src="img/logo.png" alt="" />-->
		</div>
		<div class="mui-content">
			<form id='login-form' class="mui-input-group">
				<div class="mui-input-row">
					<!--<span class="mui-icon mui-icon-contact" style="float: left;color: #25a4f4;font-weight: 700;"></span>-->
					<label>账号</label>
					<input id='userName' type="text" class="mui-input-clear mui-input" placeholder="请输入账号" name="userName">
				</div>
				<div class="mui-input-row">
					<!--<span class="mui-icon mui-icon-locked" style="float: left;color: #25a4f4;font-weight: 700;"></span>-->
					<label>密码</label>
					<input id='passWord' type="password" class="mui-input-clear mui-input" placeholder="请输入密码" name="passWord">
				</div>
				<div class="mui-input-row" style="margin-top: 15px;text-align: center;display: none;">
					<input id="chkSave" checked type="checkbox" style="width: 50px;">
					<span>保存密码</span>
				</div>
			</form>
			<div class="mui-content-padded">
				<button id='login' class="mui-btn mui-btn-block mui-btn-primary" @click='btnLogin_click'>登录</button>
			</div>
			<ul id="list" class="mui-table-view mui-table-view-chevron"></ul>
		</div>
	</div>
</template>

<script>
	//import {login} from '../../api/api.js'
	
	export default {
		data() {
			return {
				username: "",
				password: ""
			}
		},
		methods: {
			btnLogin_click: function() {
				//调用登录接口
				/*login().then(function(response) {
					if(response.meta.status === 200){
						// 跳转路由
						this.$router.push({name:'home'});
					}else {
						console.log("")
					}
				})*/
				this.$router.push({
					name: 'home'
				});
			}
		}
	}
</script>

<style scoped>
	input {
		color: #707070!important;
	}
	
	.mui-content {
		padding-top: 0 !important;
	}
	
	.bsody {
		margin: 50px 0 0 0px;
	}
	
	.bsody img {
		width: 100%;
	}
	
	.mui-input-group input,
	.mui-input-group textarea {
		width: 70%;
	}
	
	.mui-icon {
		font-size: 40px;
	}
</style>