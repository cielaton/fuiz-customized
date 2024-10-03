<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	import EmptyAnswerButton from './EmptyAnswerButton.svelte';

	export let indices: number[];

	const dispatch = createEventDispatcher<{
		answer: number;
	}>();
</script>

<div
	style:display="grid"
	style:height="100%"
	style:grid-template-columns="auto auto"
	style:gap="0.2em"
	style:padding="0.2em"
>
	{#each indices as index}
		<EmptyAnswerButton answerCount={indices.length} {index} on:click={() => dispatch('answer', index)} />
	{/each}
</div>
