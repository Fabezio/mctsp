<script>
	export let segment;
</script>

<style lang="stylus">
	nav 
		border-bottom: 1px solid rgba(255,62,0,0.1)
		font-weight: 300
		padding: 0 1em

	ul 
		margin: 0
		padding: 0

	/* clearfix */
	ul::after 
		content: ''
		display: block
		clear: both

	li 
		display: block
		float: left

	[aria-current] 
		position: relative
		display: inline-block

	[aria-current]::after 
		position: absolute
		content: ''
		width: calc(100% - 1em)
		height: 2px
		background-color: rgb(255,62,0)
		display: block
		bottom: -1px

	a 
		text-decoration: none
		padding: 1em 0.5em
		display: block
	
</style>

<nav>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Accueil</a></li>
		<li><a aria-current="{segment === 'services' ? 'page' : undefined}" href="services">Services</a></li>
		<li><a aria-current="{segment === 'groupe' ? 'page' : undefined}" href="groupe">Le Groupe</a></li>
		<li><a aria-current="{segment === 'carriere' ? 'page' : undefined}" href="carriere">Carrière</a></li>
		<li><a aria-current="{segment === 'contact' ? 'page' : undefined}" href="contact">Contact</a></li>
		<li><a aria-current="{segment === 'agents' ? 'page' : undefined}" href="agents">Accès Agents</a></li>
		<li><a aria-current="{segment === 'dashboard' ? 'page' : undefined}" href="dashboard">Dashboard</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!-- <li><a rel=prefetch aria-current="{segment === 'blog' ? 'page' : undefined}" href="blog">blog</a></li> -->
	</ul>
</nav>
