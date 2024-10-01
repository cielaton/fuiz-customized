<script>
    import * as m from '$lib/paraglide/messages.js';

    import heart from '$lib/assets/cards-heart.svg';
    import club from '$lib/assets/cards-club.svg';
    import spade from '$lib/assets/cards-spade.svg';
    import diamond from '$lib/assets/cards-diamond.svg';
</script>

<div style:height="100%" style:position="relative">
    <div
    />
    <img src="$lib/assets/LightBackground.png" alt="The light theme background"/>
    <div style:height="100%">
        <slot/>
    </div>
</div>

<style>
    img {
        height: 100%;
        width: 100%;

        inset: 0;
        position: absolute;
        overflow: hidden;
        z-index: -1;
    }
</style>
