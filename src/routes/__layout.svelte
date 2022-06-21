<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main>
	<slot />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		width: 100%;
		min-height: 100vh;
		box-sizing: border-box;
		overflow-x: hidden;
		overflow-y: auto;
	}
</style>
