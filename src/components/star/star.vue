<template>
	<div class="star" :class="starType">
		<span v-for="itemclass in itemclasses" :class="itemclass" class="star-item"></span>
	</div>
</template>
<script>
	export default {
		props: {
			size: {
				type: Number
			},
			score: {
				type: Number
			}
		},
		computed: {
			starType(){
				return 'star-' + this.size;
			}
		}
	};
</script>
<style lang="stylus" rel="stylesheet/stylus">
	@import "../../common/stylus/mixin.styl"
	.star
		font-size:0
		.star-item
			display:inline-block
			background-repeat:no-repeat
			
		&.star-48
			.star-item
				width:20px
				height:20px
				margin-right:22px
				background-size:20px 20px
				&:last-child
					margin-right:0
				&.on
					bg-imgae('star48_on')
				&.half
					bg-imgae('star48_half')
				&.off
					bg-imgae('star48_off')
		&.star-36
		&.star-24
</style>
