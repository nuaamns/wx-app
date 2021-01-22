<template>
	<view>
		<view>{{ username }}</view>
		<view v-for="one in tel">{{ one }}</view>
		<view v-if="age >= 18"><button @tap="signup()">我要报名</button></view>
		<view><input type="text" v-model="address" placeholder="djs" /></view>
		<view>{{ address }}</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			username: 'Fuck',
			tel: ['23412423432', '34345344532'],
			age: 17,
			address: ''
		};
	},
	methods: {
		signup: function() {
			uni.showToast({
				title: '点击了报名按钮'
			});
		}
	}
};
</script>

<style></style>
