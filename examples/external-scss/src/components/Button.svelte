<script>
  import { MDCRipple } from "@material/ripple";
  import { onDestroy, onMount } from "svelte";
  import { compute_rest_props } from "svelte/internal";

  let buttonEl;
  let buttonRipple;

  onMount(() => {
    buttonRipple = new MDCRipple(buttonEl);
  });

  onDestroy(() => {});
</script>

<div class="mdc-touch-target-wrapper">
  <button bind:this={buttonEl} class="mdc-button mdc-button--touch">
    <span class="mdc-button__ripple" />
    <span class="mdc-button__label">My Accessible Button</span>
    <span class="mdc-button__touch" />
  </button>
</div>

<style lang="scss" global>
    @use "@material/button/styles";
</style>
