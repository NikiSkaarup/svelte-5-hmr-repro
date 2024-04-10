<script>
	import '$lib/../app.css';
	import Button from '$lib/components/ui/button/button.svelte';
	import * as Tooltip from '$lib/components/ui/tooltip';
	import { writable } from 'svelte/store';

	let bookmarks = writable([]);

	// $effect(() => {
	// 	bookmarks.set([]);
	// });
</script>

<Tooltip.Root>
	<Tooltip.Trigger asChild let:builder>
		<Button builders={[builder]}>trigger</Button>
	</Tooltip.Trigger>
	<Tooltip.Content>
		<p>tooltip content</p>
	</Tooltip.Content>
</Tooltip.Root>
