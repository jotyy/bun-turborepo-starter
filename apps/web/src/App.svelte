<script lang="ts">
	import Button from '$lib/components/ui/button/button.svelte';
	import Counter from './lib/components/Counter.svelte';
	async function fetchGreet() {
		const response = await fetch('/api');
		const data = await response.text();
		alert(data);
	}
</script>

<main class="flex h-screen flex-col items-center justify-center space-y-6">
	<h1 class="text-3xl font-bold">Vite + Svelte + Elysia</h1>

	<Counter />

	<Button on:click={fetchGreet}>Fetch API</Button>
</main>
