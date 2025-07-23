<script>
	import { page } from '$app/state';

	const navigationOptions = [
		{
			icon: 'bar-chart-line',
			label: 'Analytics',
			href: 'analytics'
		},
		{
			icon: 'message-3-line',
			label: 'Chats',
			href: 'chats'
		},
		{
			icon: 'settings-6-line',
			label: 'Settings',
			href: 'settings'
		},
		{
			icon: 'code-view',
			label: 'Embed',
			href: 'embed'
		}
	];

	const currentPath = $derived(page.url.pathname);
</script>

<aside
	class="fixed bottom-0 flex h-fit w-full flex-row overflow-hidden bg-slate-50 px-2 py-3.5 transition-all duration-200 ease-linear hover:w-40 md:top-1/2 md:left-4 md:w-16 md:-translate-y-1/2 md:flex-col md:rounded-4xl"
>
	<a href="/" class="hidden flex-col items-center gap-4 p-2 md:flex md:flex-row">
		<div class="flex h-8 w-8 shrink-0 items-center justify-center rounded-full bg-slate-100">
			<i class="ri-speak-ai-line text-xl"></i>
		</div>
		<span>Juno</span>
	</a>
	<hr class="mb-4 border-slate-100" />
	<nav class="flex w-full md:flex-col">
		{#each navigationOptions as { icon, label, href }}
			<a
				{href}
				class="flex w-full flex-col items-center gap-4 gap-y-2 p-2 opacity-50 md:flex-row {currentPath.includes(
					href
				)
					? 'opacity-100'
					: ''}"
			>
				<div
					class="flex h-10 w-10 shrink-0 items-center justify-center rounded bg-slate-100 md:h-8 md:w-8"
				>
					<i class="ri-{icon} text-2xl md:text-xl"></i>
				</div>
				<span class="text-xs md:text-base">{label}</span>
			</a>
		{/each}
	</nav>
</aside>
