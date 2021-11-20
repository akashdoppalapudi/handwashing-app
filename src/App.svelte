<script>
    import Timer from "./Timer.svelte";
    import HowTo from "./HowTo.svelte";

    let audio;

    const timerEnds = () => {
        audio.play();
    }
</script>

<style>
    h1 {
        text-align: center;
    }
</style>

<h1>Hand Washing App</h1>
<Timer on:end={timerEnds} />
<HowTo />

<h3>
    <a href="https://www.who.int/teams/integrated-health-services/infection-prevention-control" target="_blank">Picture Source</a>
</h3>
<h3><a href="https://freesound.org/people/metrostock99/sounds/345086/" target="_blank">Sound Source</a></h3>

<audio bind:this={audio}>
    <source src="sound.wav" />
</audio>
