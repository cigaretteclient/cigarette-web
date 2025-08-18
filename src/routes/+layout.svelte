<script lang="ts">
	import "../app.css";
	import favicon from "$lib/assets/favicon.svg";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Cigarette Client</title>
	<meta
		name="description"
		content="A next-generation Minecraft hacked client for Hypixel minigames. Completely free and open source."
	/>
	<meta name="og:title" content="Cigarette Client" />
	<meta name="og:url" content="https://cigarette.dev" />
	<meta
		name="og:description"
		content="A next-generation Minecraft hacked client for Hypixel minigames. Completely free and open source."
	/>
	<meta name="og:image" content={favicon} />
	<link rel="canonical" href="https://cigarette.dev" />
</svelte:head>

<div class="font-os fixed z-10 h-full w-full overflow-auto bg-slate-950 text-white">
	<div
		class="fixed z-20 flex h-16 w-full items-center bg-slate-900/90 p-4 shadow-sm shadow-white backdrop-blur-xs"
	>
		<a href="/" class="text-2xl font-extrabold">Cigarette Client</a>
	</div>
	<div class="h-16 w-0.5"></div>
	<div class="p-6">{@render children?.()}</div>
</div>
