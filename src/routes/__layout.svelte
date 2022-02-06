<script>
  import PageTransition from "$lib/PageTransition.svelte";
</script>

<ul>
  <li><a href="/">Home</a></li>
  <li><a href="/contact">Contact</a></li>
</ul>

<PageTransition>
  <div class="card">
    <slot />
  </div>
</PageTransition>

<style>
  .card {
    border: 1px solid grey;
    padding: 40px;
    max-width: 600px;
  }
</style>
