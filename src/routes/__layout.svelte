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
	<link
		href="https://fonts.googleapis.com/css2?family=JetBrains+Mono&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<main>
	<header class="flex flex-row relative cornerTop">
		<div class="flex flex-row relative justify-between uppercase border p-4 w-full cornerBottom">
			<div>machined monster</div>
			<div>in progress ...</div>
		</div>
	</header>
	<div class="flex flex-1 relative cornerTop my-4">
		<div class="flex flex-1 relative cornerBottom border">
			<slot />
		</div>
	</div>
	<footer>
		<span>44exa</span>
		<span>{new Date().getUTCFullYear()}</span>
	</footer>
</main>

<style>
	main {
		@apply flex flex-1 flex-col p-4 w-full max-w-xl my-0 mx-auto;
		height: 100vh;
		height: calc(var(--vh, 1vh) * 100);
	}

	footer {
		@apply flex flex-row justify-between;
	}

	.cornerTop:before {
		position: absolute;
		left: 0px;
		top: 0px;
		content: '';
		border-top: 20px solid white;
		border-right: 20px solid transparent;
	}

	.cornerTop:after {
		position: absolute;
		left: -1px;
		top: -1px;
		content: '';
		border-top: 20px solid black;
		border-right: 20px solid transparent;
	}

	.cornerBottom:before {
		position: absolute;
		right: -1px;
		bottom: -1px;
		content: '';
		border-bottom: 20px solid white;
		border-left: 20px solid transparent;
	}

	.cornerBottom:after {
		position: absolute;
		right: -2px;
		bottom: -2px;
		content: '';
		border-bottom: 20px solid black;
		border-left: 20px solid transparent;
	}
</style>
