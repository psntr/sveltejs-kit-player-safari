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
	<p>Demonstrates an issue where <code>&lt;media-theme&gt;</code> controls work on client-side navigation on all browsers except on Safari Desktop when other HTML is present than the player component.</p>
	<p><strong>Also note:</strong> <code>&lt;media-theme&gt;</code> do not init on full page load </p>
	<Player />
</div>
