<script>
	export let page = 'about';
	import { Tween, Spring } from 'svelte/motion';
	import { cubicOut } from 'svelte/easing';
	import { fade, slide } from 'svelte/transition';
	let progress = new Tween(0, { duration: 1000, easing: cubicOut });
</script>

<div class=" flex flex-col items-center justify-center gap-5">
	<h1 class=" bg-slate-600">{page}</h1>

	<a href="/">home page</a>
	<div in:fade out:slide>Привіт, світ!</div>
	{#each [{ id: 1, text: 'Анімація!' }] as item (item.id)}
		<div>{item.text}</div>
	{/each}
	<div in:fade={{ duration: 1000 }}>Повільна поява</div>
	<div style="width: {progress}%;">Прогрес</div>
</div>
