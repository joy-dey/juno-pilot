<script>
	import { blur } from 'svelte/transition';
</script>

<svelte:head>
	<title>Analytics</title>
</svelte:head>

<div class="flex h-svh flex-col items-center justify-center gap-1" transition:blur>
	<i class="ri-bar-chart-line text-4xl"></i>
	<h1 class="text-2xl font-semibold text-slate-800">Analytics</h1>
	<p class="text-slate-500">Aha! You are currently at the Analytics page</p>
</div>
