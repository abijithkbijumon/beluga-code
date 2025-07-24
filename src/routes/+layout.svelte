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


<main>
  <slot /> <!-- 👈 This is where +page.svelte content appears -->
</main>

