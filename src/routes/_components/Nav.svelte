<nav>
	<ul>
		<li><a class='{segment === undefined ? "selected" : ""}' href='.'>home</a></li>
		<!-- <li><a class='{segment === "about" ? "selected" : ""}' href='about'>about</a></li> -->

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li><a rel=prefetch class='{segment === "blog" ? "selected" : ""}' href='blog'>blog</a></li> -->
	</ul>
</nav>

<script>
	export let segment
</script>

<style type="text/scss">
	nav {
		border-bottom: 1px solid $gray-light;
		padding: 0 3rem;
		margin: 0 0 5rem;
		background-color: rgba(255, 158, 11, 0.1);
	}
	ul {
		display: flex;
		margin: 0;
		padding: 0;
		list-style: none;
	}
	.selected {
		position: relative;
	}
	.selected::after {
		position: absolute;
		content: '';
		width: 100%;
		height: 3px;
		background-color: rgb(255, 158, 11);
		display: block;
		bottom: -1px;
	}
	a {
		text-decoration: none;
		padding: 1rem 3rem;
		display: block;
		text-align: center;
	}
</style>
