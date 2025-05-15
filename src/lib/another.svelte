<script lang="ts">
	import type { ComponentProps } from 'svelte';
	import SomeComponent from './component.svelte';

	let { extraProps }: { extraProps: Partial<ComponentProps<typeof SomeComponent>> } = $props();
</script>

<SomeComponent {...extraProps} />

<SomeComponent {...extraProps}>It has a child so now it shuts up.</SomeComponent>

<SomeComponent {...extraProps} children={undefined} />
