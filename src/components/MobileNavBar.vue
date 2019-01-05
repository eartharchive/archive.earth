1<template>
<div>
	<div class="menu-overlay" v-if="menu"></div>
	<nav class="mobile-nav">
    <div class="logo">
      <router-link to="/">
        <img src="/assets/archive-earth-logo.svg" alt="archive-earth-logo">
      </router-link>
    </div>
		
		<div class="menu-toggle-btn" @click="toggleMenu">
			<b-icon
					icon="menu"
					size="is-large"
					
					>
			</b-icon>
		</div>

    <ul class="menu" v-if="menu">
      <li>
        <router-link to="/about" @click.native="toggleMenu">About</router-link>
      </li>
      <li>
        <router-link to="/news" @click.native="toggleMenu">News</router-link>
      </li>
      <li>
        <router-link to="/follow" @click.native="toggleMenu">Follow</router-link>
      </li>
    </ul>
  </nav>
</div>
  
</template>

<script>
export default {
	data(){
		return {
			menu: false,
		}
	},

	methods: {
		toggleMenu(){
			this.menu = !this.menu
			console.log(this.menu)
		}
	}
};
</script>

<style>
.menu-overlay{
	position: absolute;
	width: 100%;
	height: 100%;
	z-index: 10;
	background-color: #f8f8f8;
	opacity: .95;
}
.mobile-nav{
	position: absolute;
	z-index: 10;
	width: 100%;
}

.mobile-nav .logo{
	float: left;
	width: 120px;
	height: 120px;
	display: flex;
	align-items: center;
	margin-left: 10px;
}

.mobile-nav .menu-toggle-btn{
	float: right;
	padding: 35px 4.5% 0 0;
	color: #999999;
}

.mobile-nav .menu{
	clear: both;
}

.mobile-nav .menu li a{
    color: rgba(26, 51, 21, 1.0);
		font-size: 30px;
		font-weight: 700;
}

.mobile-nav .menu li {
    margin-bottom: 20px;
}

</style>
