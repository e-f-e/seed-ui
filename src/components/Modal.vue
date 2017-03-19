<style lang='scss' scoped>
	.modal {
		.modal-content {
			h4 {
				text-align: left;
			}
		}
	}

	.open {
		z-index: 1003;
    	display: block;
    	opacity: 1;
    	transform: scaleX(1);
    	top: 10%;
	}
</style>
<template>
	<!-- Modal Structure -->
  	<div class="modal" :class='modalClass'>
    	<div class="modal-content">
      		<h4>{{title}}</h4>
      		<div>
      			<slot></slot>
      		</div>
    	</div>
    	<div class="modal-footer">
      		<a href="javascript:void(0);" v-on:click='onOk' class=" modal-action modal-close waves-effect waves-green btn-flat">{{okText}}</a>
      		<a href="javascript:void(0);" v-on:click='onCancel' class=" modal-action modal-close waves-effect waves-green btn-flat">{{cancelText}}</a>
    	</div>
  </div>
</template>
<script>
	export default {
		props: {
			isShow: {
				type: Boolean,
				default: false
			},
			title: {
				type: String
			},
			okText: {
				type: String,
				default: 'yes'
			},
			cancelText: {
				type: String,
				default: 'cancel'
			}
		},
		computed: {
			modalClass () {
				return {
					open: this.isShow
				};
			}
		},
		methods: {
			onOk () {
				this.$emit('ok');
			},
			onCancel () {
				this.$emit('cancel');
			}
		}
	}
</script>