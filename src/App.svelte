<script>
	import { Router, Route } from '@c0ldra1n/svero';
	import Header from './Header.svelte';
	import Index from './pages/Index.svelte';
	import About from './pages/About.svelte';
</script> 

<style>
    :global(body) {
		/* this will apply to <body> */
		margin: 0;
		padding: 0;
	}

	.container { 
		width: 80%;
		margin: 4em auto;
	}
</style>
<Header/>
<div class="container">
	<Router>
		<Route path="/" exact component={Index} />
		<Route path="/about" component={About} />
	</Router>
</div>