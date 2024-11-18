<script>
  import { onMount } from "svelte";

  let currentDate = '';

  onMount(() => {
    const date = new Date();
    currentDate = new Intl.DateTimeFormat('en-US', {
      weekday: 'long',
      year: 'numeric',
      month: 'long',
      day: 'numeric'
    }).format(date);
  });
</script>

<main>
  <p>{currentDate}</p>
</main>
