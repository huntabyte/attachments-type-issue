<script lang="ts">
	import type { HTMLAttributes } from 'svelte/elements';

	let {
		children,
		ref = $bindable(),
		...restProps
	}: HTMLAttributes<HTMLElement> & {
		ref?: HTMLElement;
	} = $props();
</script>

<div bind:this={ref} class="component" {...restProps}>
	{@render children?.()}
</div>
