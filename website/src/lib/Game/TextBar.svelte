<script lang="ts">
	import * as m from '$lib/paraglide/messages.js';

	import { createEventDispatcher } from 'svelte';
	import FancyButton from '../FancyButton.svelte';
	export let text: string;
	export let topShadow = false;
	export let showNext = false;

	const dispatch = createEventDispatcher<{ next: undefined }>();

	export let heading = false;
</script>

<div
	style:background="var(--background-color)"
	style:display="flex"
	style:line-height="1.2"
	style:align-items="center"
	style:justify-content="center"
	style:padding="0.2em 0.4em"
	style:border-bottom="0.15em solid currentcolor"
	style:border-top={topShadow ? '0.15em solid currentcolor' : ''}
	style:text-align="center"
	style:z-index="1"
>
	<div
		style:flex="1"
		style:font-size="3em"
		style:font-weight="bold"
		style:word-break="break-word"
		style:font-family={heading ? 'Poppins' : 'inherit'}
	>
		{text}
	</div>
	{#if showNext}
		<div style:font-size="1.2em" style:font-family="Poppins">
			<FancyButton on:click={() => dispatch('next')}>
				<div style:padding="0.2em 0.4em">{m.next()}</div>
			</FancyButton>
		</div>
	{/if}
</div>
