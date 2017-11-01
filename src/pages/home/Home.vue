
<template>
  <div>
  	<div class="header">
  	<b></b>
 		<indexheader />
 		<nav>{{msg}}</nav>
 		
  	</div>
 
  	<lunbo/>
  
  </div>
</template>

<script>
import indexheader from "./header.vue";
import lunbo from "./lunbo.vue";
import "../../../node_modules/swiper/dist/css/swiper.css";

export default {
  data () {
    return {
      msg: '北京'
    }
  },
  components:{
  	indexheader,
  	lunbo
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	
	.header{
		width:100%;height:.4rem;background: #fa0;
		position: relative;
	}
	.header>b{
		width:.3rem;position: absolute;background: #fff;margin-top: 0.05rem;
	}
	.header>b::before,.header>b::after{
		content: "";display: block;position: absolute;width:.1rem;height:0.02rem;background: #000;top:.14rem;left:.1rem;
	}
	.header>b::before{
		transform:rotate(-45deg);transform-origin: left;
	}
	.header>b::after{
		transform:rotate(45deg);transform-origin: left;
	}
	.header>nav{
		position: absolute;right: 5%;top:50%;transform:translate(0,-50%)
	}
	.header>nav::after{
		content: "";position: absolute;top:38%;right: -30%;
		width:0rem;height:0rem;
	  border-bottom: .1rem solid #fff;
	  border-right: .05rem solid transparent;
	  border-left: .05rem solid transparent;
	}
</style>
