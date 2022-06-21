<script context="module">
	export const prerender = true;
</script>

<script>
	import Map from '$lib/Map.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Map />
	<svg class="cloud" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" xmlns:xlink="http://www.w3.org/1999/xlink" enable-background="new 0 0 512 512">
		<path d="m467.8,154c-6.6-57.3-60.1-100.9-126.1-100.9-13.6,0-26.8,1.9-39.5,5.6-23.6-29.1-61.6-46.7-102.9-46.7-70,0-126.9,50.6-126.9,112.7 0,3.3 0.2,6.6 0.5,9.9-37.5,20.2-61,56.5-61,96.3 0,50.3 36.3,93.7 90.4,108 11,2.9 22.1-3.6 25-14.5 2.9-10.9-3.6-22.1-14.5-25-35.9-9.5-60.1-37.1-60.1-68.5 0-28 19.8-53.6 50.4-65.4 9.8-3.8 15.2-14.4 12.4-24.5-1.6-5.7-2.4-11-2.4-16.3 0-39.6 38.6-71.9 86-71.9 33.1,0 62.8,15.6 77.4,40.7 5.2,8.9 16.2,12.6 25.8,8.5 12.3-5.3 25.6-8 39.2-8 46.4,0 84.9,31.6 85.9,70.3 0.2,5.9 2.9,11.5 7.5,15.3 16.8,13.7 26,31.9 26,51.3 0,34.8-31,65.4-72.2,70.9-11.2,1.5-19,11.8-17.5,23 1.4,10.2 10.1,17.7 20.2,17.7 0.9,0 1.8-0.1 2.8-0.2 62.6-8.4 107.8-55.3 107.8-111.4 0-28.5-12.4-56.1-34.2-76.9z"/>
		<path d="m174.4,345.9c-7.9,8-7.9,20.9 0.1,28.9 22.9,22.7 53,34.1 83.2,34.1 30.4,0 60.8-11.5 84-34.5 8-7.9 8-20.9 0.1-28.9-8-8-20.9-8-28.9-0.1-30.3,30.1-79.5,30.3-109.6,0.4-8.1-8-21-7.9-28.9,0.1z"/>
		<path d="m377.6,411.3c-66.7,66.3-174.9,66.7-241.2,0.9-8-7.9-20.9-7.9-28.9,0.1-7.9,8-7.9,20.9 0.1,28.9 40.9,40.6 94.7,60.9 148.6,60.9 54.3,0 108.7-20.6 150.2-61.8 8-7.9 8-20.9 0.1-28.9-8-8-20.9-8.1-28.9-0.1z"/>
		<path d="m282.6,290.5c0-13.5-11-24.5-24.5-24.5-13.5,0-24.5,11-24.5,24.5s11,24.5 24.5,24.5c13.5,0 24.5-11 24.5-24.5z"/>
	</svg>
	<div class="flex-2">
		<div class="intro">
			<h2>Erfaren. Solid. Fremtidsrettet.</h2>
			<div class="flex-2">
				<span>
					Snart 20 år som IT-avdeling til norske kommuner.
					Med et stadig bredere spekter å spille på i digitaliseringskappløpet.
				</span>
				<div class="flex-2 buttons">
					<a class="button-fill" href="/tjenester">Tjenester</a>
					<a class="button-border" href="/om-oss">Om oss</a>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	section {
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		align-items: flex-start;
		flex: 1;
		background-color: var(--pure-black);
		color: var(--pure-white);
	}
	.cloud {
		position: absolute;
		top: 8rem;
		left: 5rem;
		width: 20em;
		fill: var(--accent-color);
		transform: rotate(-15deg);
	}
	.cloud path:nth-child(4) {
		fill: #000;
		animation: pulse 3s linear 0s infinite;
	}
	.cloud path:nth-child(2) {
		fill: #000;
		animation: pulse 3s linear .25s infinite;
	}
	.cloud path:nth-child(3) {
		fill: #000;
		animation: pulse 3s linear .5s infinite;
	}

	@keyframes pulse {
		0% {
			fill: #000;
		}
		50% {
			fill: var(--accent-color);
		}
		75% {
			fill: #000;
		}
	}
	.flex-2 {
		position: relative;
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr;
	}
	.intro {
		margin: 4rem;
	}
	h2 {
		font-size: 4rem;
		text-transform: uppercase;
		font-weight: 900;
		line-height: 1.2;
	}
	span {
		line-height: 1.5;
	}
	a:hover {
		text-decoration: none;
	}
	.buttons {
		align-items: center;
		gap: 1.5rem;
	}
	.buttons a {
		padding: 1rem 2rem;
		font-size: 1rem;
		text-align: center;
		font-weight: 600;
	}
	.button-fill {
		background: var(--accent-color);
		border: 2px solid var(--accent-color);
		color: var(--pure-black);
	}
	.button-border {
		border: 2px solid var(--accent-color);
		color: var(--accent-color)
	}
</style>
