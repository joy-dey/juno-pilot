<script>
	import { blur } from 'svelte/transition';
</script>

<svelte:head>
	<title>Chats</title>
</svelte:head>

<div class="flex h-svh flex-col items-center justify-center gap-1" transition:blur>
	<i class="ri-message-3-line text-4xl"></i>
	<h1 class="text-2xl font-semibold text-slate-800">Chats</h1>
	<p class="text-slate-500">Aha! You are currently at the Chats page</p>
</div>
