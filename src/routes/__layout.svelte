<script lang="ts">
	import '../app.css';
	if (typeof window !== 'undefined') {
		//here `window` is available
		window.addEventListener('resize', () => {
			// We execute the same script as before
			let vh = window.innerHeight * 0.01;
			document.documentElement.style.setProperty('--vh', `${vh}px`);
		});
	}
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono&display=swap" rel="stylesheet">
</svelte:head>

<main>
	<header>
		<div>machined</div>
		<div>monster</div>
	</header>
	<slot />
	<footer>
		<span>{new Date().getFullYear()}</span>
		<span>work in progress...</span>
	</footer>
</main>

<style>
	main {
		@apply flex flex-1 flex-col p-4 w-full max-w-xl my-0 mx-auto;
		height: 100vh;
		height: calc(var(--vh, 1vh) * 100);
	}

	header {
		@apply flex flex-row justify-between uppercase
	}

	footer {
		@apply flex flex-row justify-between
	}

</style>
