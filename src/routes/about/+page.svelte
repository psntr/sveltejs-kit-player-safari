<script>
	import { resolve } from '$app/paths';
 	import 'hls-video-element';
  	import 'player.style/sutro';
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
	<div style="border: red 1px solid"><Player /></div>
	<p>Without component and using Packaged Method</p>
	<div style="border: blue 1px solid">
		<media-theme-sutro style="width: 100%;">
		  <hls-video
		    slot="media"
		    src="https://stream.mux.com/fXNzVtmtWuyz00xnSrJg4OJH6PyNo6D02UzmgeKGkP5YQ.m3u8"
		    playsinline
		    crossorigin="anonymous"
		  ></hls-video>
		</media-theme-sutro>
	</div>
</div>
