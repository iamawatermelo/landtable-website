<script lang="ts">
  import type { Snippet } from 'svelte';

  let {
    children = undefined
  }: {
    children: Snippet<[]> | undefined
  } = $props();
  
  import '../app.scss';
  import '$lib/utility.scss';
</script>

{@render children?.()}