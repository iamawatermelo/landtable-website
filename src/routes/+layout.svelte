<script lang="ts">
  import Landtable from '$lib/icons/Landtable.svg?component';
  import type { Snippet } from 'svelte';

  let {
    children = undefined
  }: {
    children: Snippet<[]> | undefined
  } = $props();
  
  import '../app.scss';
  import '$lib/utility.scss';
</script>

<nav>
  <ul>
    <li><a href="/" class="icon"><Landtable /><span>landtable</span></a></li>
    <div>
      <li><a href="/">Platform</a></li>
      <li><a href="/">Proxy</a></li>
      <li><a href="/">Docs</a></li>
      <li><a href="/">Hack Club log in</a></li>
    </div>
  </ul>
</nav>

{@render children?.()}

<style lang="scss">
  nav {
    position: sticky;
    height: 4em;
    border-bottom: 1px solid rgb(var(--fg-color), 0.2);
    padding: 1em;
    
    ul {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      height: 100%;
      max-width: 100em;
      margin: auto;
      padding: unset;
      list-style: none;
      
      li {
        margin: unset;
        padding: unset;
      }
      
      div {
        display: flex;
        flex-direction: row;
        gap: 1em;
      }
      
      .icon {
        display: flex;
        align-items: center;
        font-size: 1.5em;
        gap: .25em;
        text-decoration: none;
        
        :global(svg) {
          height: 1em;
          width: 1em;
        }
        
        span {
          display: block;
        }
      }
    }
  }
</style>