<script>
	import Button from "../lib/Button.svelte";
	
	let offset = 0;

	function onKeyDown(e) {
		switch (e.keyCode) {
			case 37:
				offset -= 1;
				break;
			case 39:
				offset += 1;
				break;
		}
	}
</script>

<main class="flex h-screen items-center overflow-hidden">
	<p
		class="whitespace-nowrap font-serif text-7xl selection:bg-purple-50 relative"
		style="right: {offset}cm"
	>
		Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
		labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
		laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
		voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
		non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
	</p>
	<Button style="right: {offset}cm">play</Button>
	<Button style="right: {offset}cm">play</Button>
</main>

<svelte:window on:keydown|preventDefault={onKeyDown} />
