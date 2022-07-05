<script context="module" lang="ts">
	export const prerender = true;
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<img src="/images/dino.svg" alt="Chromium T-rex"/>
	<span class=" font-bold mt-8">rraawwrr!</span>
</section>

<style>
	section {
		@apply flex flex-col flex-1 justify-center items-center;
	}
</style>
