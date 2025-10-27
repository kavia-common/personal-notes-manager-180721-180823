<script lang="ts">
  import TopBar from '$lib/components/TopBar.svelte';
  import Sidebar from '$lib/components/Sidebar.svelte';
  import NoteEditor from '$lib/components/NoteEditor.svelte';
  import { notesStore } from '$lib/stores/notes';

  function handleNew() {
    notesStore.createNote();
  }
</script>

<svelte:head>
  <title>Ocean Notes</title>
  <meta name="description" content="A modern notes app with a clean Ocean Professional theme." />
</svelte:head>

<div class="page">
  <TopBar onNew={handleNew} />
  <div class="content">
    <Sidebar />
    <div class="main">
      <NoteEditor />
    </div>
  </div>
</div>

<style>
  .page {
    display: grid;
    grid-template-rows: auto 1fr;
    min-height: 100vh;
    background: linear-gradient(180deg, color-mix(in oklab, var(--primary-500) 3%, transparent), transparent);
  }
  .content {
    display: grid;
    grid-template-columns: 360px 1fr;
    gap: 0;
    height: 100%;
  }
  .main {
    background: var(--surface);
  }
  @media (max-width: 900px) {
    .content {
      grid-template-columns: 1fr;
    }
  }
</style>
