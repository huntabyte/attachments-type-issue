<script lang="ts">
	import type { ComponentProps } from 'svelte';
	import Component from './component.svelte';

	let { extraProps }: { extraProps: { component?: Partial<ComponentProps<typeof Component>> } } =
		$props();
</script>

<Component {...extraProps?.component} />
