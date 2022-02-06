<script>
  import { fly } from "svelte/transition";
  import { page } from "$app/stores";

  let duration = 3000;
  let transitionX = 700;
</script>

<div style:display="grid" style:overflow="hidden">
  {#key $page.url.pathname}
    <div
      in:fly={{ x: transitionX, duration: duration }}
      out:fly|local={{ x: -transitionX, duration }}
      style:grid-column="1 / 1"
      style:grid-row="1 / 1"
    >
      <slot />
    </div>
  {/key}
</div>
