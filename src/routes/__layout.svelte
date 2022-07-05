<script lang="ts">
	import '../app.css';
</script>

<svelte:head>
  <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono&display=swap" rel="stylesheet">
</svelte:head>

<main>
	<slot />
	<footer>
		<span>©{new Date().getFullYear()} truclr</span>
	</footer>
</main>

<style>
	main {
		@apply flex flex-1 flex-col p-4 w-full h-screen max-w-5xl my-0 mx-auto;
	}

	footer {
		@apply flex flex-col justify-center items-center;
	}

</style>
