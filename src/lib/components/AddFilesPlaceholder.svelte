<script>
	import { getContext } from 'svelte';

	export let title = '';
	const i18n = getContext('i18n');
</script>

<div class="  text-center text-6xl mb-3">📄</div>
<div class="text-center dark:text-white text-2xl font-semibold z-50">
	{#if title}
		{title}
	{:else}
		{$i18n.t('Add Files')}
	{/if}
</div>

<slot
	><div class=" mt-2 text-center text-sm dark:text-gray-200 w-full">
		{$i18n.t('Drop any files here to add to the conversation')}
	</div>
</slot>
