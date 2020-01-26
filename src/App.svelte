<script>
  import Slider from "./slider.svelte";

  let boolean = false;
</script>

<div>
  <Slider bind:active={boolean} />

  <h1>valor >> {boolean ? 'ligado' : 'desligado'}</h1>
</div>
