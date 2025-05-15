<script lang="ts">
	import type { HTMLAttributes } from 'svelte/elements';

	let { children, ...restProps }: HTMLAttributes<HTMLElement> = $props();
</script>

<div {...restProps}>
	{@render children?.()}
</div>
