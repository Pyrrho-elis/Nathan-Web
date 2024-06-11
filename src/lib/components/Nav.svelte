<script>
	import { toggleMode } from 'mode-watcher';
	import { Sun, Moon } from 'svelte-radix';
    import Button from './ui/button/button.svelte';
</script>

<nav class="sticky flex items-center justify-between p-4 text-xl backdrop-blur-sm m-4">
	<h1 class="text-3xl font-bold"><a href="/">Nathan</a></h1>
	<ul class="flex gap-8 items-center mx-4 text-xl">
		<li><a href="/">Home</a></li>
		<li><a href="/projects">Projects</a></li>
		<li><a href="/me">About</a></li>
        <li>
			<Button on:click={toggleMode} variant="outline" size="icon">
				<Sun
					class="scale-100 transition-all dark:-rotate-90 dark:scale-0"
				/>
				<Moon
					class="absolute h-[1.2rem] w-[1.2rem] rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100"
				/>
			</Button>
		</li>
	</ul>
</nav>
