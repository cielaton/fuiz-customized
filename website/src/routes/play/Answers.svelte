<script lang="ts">
	import Answers from '$lib/Game/Answers.svelte';
	import EmptyAnswers from '$lib/Game/EmptyAnswers.svelte';
	import TextBar from '$lib/Game/TextBar.svelte';
	import MediaDisplay from '$lib/MediaDisplay.svelte';
	import NiceBackground from '$lib/NiceBackground.svelte';
	import type { Media, TextOrMedia } from '$lib/types';
	import Topbar from './Topbar.svelte';

	export let questionText: string;
	export let name: string;
	export let score: number;
	export let media: undefined | Media;
	export let showAnswers: boolean;
	export let answers: (TextOrMedia | undefined)[];
</script>

<div style:height="100%" style:width="100%" style:display="flex" style:flex-direction="column">
	<div>
		<Topbar {name} {score} />
		{#if showAnswers}
			<TextBar text={questionText} />
		{/if}
	</div>
	<div style:flex="1" style:height="100%">
		<NiceBackground>
			<div style:height="100%" style:display="flex" style:flex-direction="column">
				{#if media && showAnswers}
					<div style:height="40dvh">
						<MediaDisplay {media} fit="contain" />
					</div>
				{/if}
				{#if !showAnswers}
					<EmptyAnswers indices={[...new Array(answers.length).keys()]} on:answer />
				{:else}
					<div style:flex="1" style:font-size="1.5em">
						<Answers
							answers={answers.map((t) => ({ text: t?.Text, correct: undefined }))}
							on:answer
						/>
					</div>
				{/if}
			</div>
		</NiceBackground>
	</div>
</div>
