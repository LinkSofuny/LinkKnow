<template>
	<view>
		<view class="">
			<slot></slot>
			<view 
			v-if="showRefresh" @click="$emit('refresh')"
			class="flex align-center justify-center py-2 text-main " hover-class="text-main-hover">
			</view>
		</view>
		<view class="f-divider" v-if="showGap" >
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			showRefresh: {
				type: Boolean,
				default: true
			},
			showGap: {
				type: Boolean,
				default: true
			},
			title: {
				type: String,
				default: null
			}
		},
	}
</script>

<style>
</style>
