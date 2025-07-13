<script lang="ts">
  import { onMount } from 'svelte';
  import { goto } from '$app/navigation';

  onMount(() => {
    const handler = (e: KeyboardEvent) => {
      if (e.ctrlKey && e.key === '1') goto('/code');
      if (e.ctrlKey && e.key === '2') goto('/compute');
      if (e.ctrlKey && e.key === '3') goto('/chat');
    };

    window.addEventListener('keydown', handler);
    return () => window.removeEventListener('keydown', handler);
  });
</script>

<nav style="padding: 1rem; background: #f0f0f0;">
  <a href="/tab1" style="margin-right: 1rem;">Tab 1</a>
  <a href="/tab2">Tab 2</a>
</nav>

<main style="padding: 1rem;">
  <slot /> <!-- 👈 This is where +page.svelte content appears -->
</main>

