<script>
	import { page } from '$app/stores';
	import logo from './logo-white.png';
</script>

<header>
	<div class="left">
		<a href="/">
			<img src={logo} alt="Ikomm" />
		</a>
	</div>

	<nav>
		<ul>
			<li class:active={$page.url.pathname === '/tjenester'}><a sveltekit:prefetch href="/tjenester">Tjenester</a></li>
			<li class:active={$page.url.pathname === '/om-oss'}>
				<a sveltekit:prefetch href="/om-oss">Om oss</a>
			</li>
			<li class:active={$page.url.pathname === '/jobb'}>
				<a sveltekit:prefetch href="/jobb">Jobb</a>
			</li>
			<li class:active={$page.url.pathname === '/academy'}>
				<a sveltekit:prefetch href="/academy">Academy</a>
			</li>
		</ul>
	</nav>

	<div class="right">
		<a sveltekit:prefetch href="/kontakt">Kontakt oss</a>
	</div>
</header>

<style>
	header {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		z-index: 9;
	}

	.left, .right {
		margin: 0 3rem;
	}

	.left a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.left img {
		height: 1.5rem;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li.active::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--accent-color);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--pure-white);
		font-size: 1rem;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}

</style>
