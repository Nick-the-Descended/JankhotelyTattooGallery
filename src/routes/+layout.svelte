<script>
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import { locales, getLocale, setLocale } from '$lib/paraglide/runtime';

	let { children } = $props();
	let current = getLocale();

	function switchLocale(locale) {
		if (locale === current) return;
		// Let Paraglide handle persisting locale (cookie/global) and reload
		setLocale(locale);
	}
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<!-- Simple language switcher -->
<nav class="lang-switcher">
	{#each locales as locale}
		<button
			class:selected={locale === current}
			onclick={() => switchLocale(locale)}
			title={`Switch to ${locale}`}
		>
			{locale === 'en' ? 'EN' : locale === 'ka-ge' ? 'KA' : locale}
		</button>
	{/each}
</nav>

{@render children?.()}

<style>
	.lang-switcher {
		position: fixed;
		top: 0.75rem;
		right: 0.75rem;
		display: flex;
		gap: 0.25rem;
		z-index: 50;
	}
	.lang-switcher button {
		padding: 0.25rem 0.5rem;
		border-radius: 0.375rem;
		border: 1px solid rgba(0,0,0,0.15);
		background: rgba(255,255,255,0.8);
		backdrop-filter: blur(6px);
		cursor: pointer;
		font-weight: 600;
	}
	.lang-switcher button.selected {
		background: #111827;
		color: white;
		border-color: #111827;
	}
</style>
