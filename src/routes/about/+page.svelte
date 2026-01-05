<script>
	import { resolve } from '$app/paths';
	import Player from '../Player.svelte';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
	<h1>About this app</h1>
	<p>Demonstrates an issue where `<media-theme>` controls work on full page load but break on client-side navigation on Safari Desktop.
</p>
	<Player />
</div>
