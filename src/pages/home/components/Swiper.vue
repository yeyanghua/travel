<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
			<!-- slides -->
			<swiper-slide v-for="item of swiperList">
				<img class="swiper-img" :src="item.imgUrl" :key="item.id"/>
			</swiper-slide>
			<!-- Optional controls -->
			<div class="swiper-pagination" slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data() {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop:true
				},
				swiperList: [{
				id: '0001',
				imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/b6/f9d9eac3d25e8d02.jpg_640x200_f10641be.jpg'
			},{
				id: '0002',
				imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/4c/9f170839b372c302.jpg_640x200_68e5cc5b.jpg'
			},{
				id: '0003',
				imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/22/8db8a7944519e902.jpg_890x330_efa072a7.jpg'
			}]
			}
		
		}
	}
</script>

<style lang="stylus" scoped="scoped">
 .wrapper>>>.swiper-pagination-bullet-active
	    background: #fff
	.wrapper
	  overflow:hidden
	  height:0
	  width:100%
	  padding-bottom: 31.25%
	  .swiper-img 
	   width:100%
</style>