<script lang="ts">
  import '../app.css';
  let { children } = $props();
</script>

<main class="root">
  {@render children()}
</main>

<style>
  .root {
    display: block;
    min-height: 100vh;
    background: var(--background);
  }
</style>
