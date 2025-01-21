<script>
	import { slide } from 'svelte/transition';
</script>

<div
	in:slide
	out:slide
	class="flex h-screen w-full flex-col items-center justify-center gap-5 bg-slate-400"
>
	<h1>Welcome to SvelteKit</h1>
	<p>
		Visit <a href="https://svelte.dev/docs/kit">svelte.dev/docs/kit</a> to read the documentation
	</p>
	<a href="/about">Aboute page</a>
</div>
