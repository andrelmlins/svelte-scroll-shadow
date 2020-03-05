<script>
  import { onMount, onDestroy } from 'svelte';
  import ResizeObserver from 'resize-observer-polyfill';

  export let style = '';
  export let styleSubcontainer;
  export let scrollColor = '#c5c5c5';
  export let scrollPadding = '0px';
  export let scrollWidth = '8px';
  export let scrollColorHover = '#a6a6a6';
  export let shadow =
    '0 2px 4px rgba(0, 0, 0, 0.2) inset, 0 -2px 4px rgba(0, 0, 0, 0.2) inset';
  export let isShadow = false;

  $: shadow = isShadow ? shadow : 'none';

  let scroll = false;
  let component = null;
  let RO = null;

  onMount(() => {
    RO = new ResizeObserver(() => {
      if (component.clientHeight < component.scrollHeight) {
        scroll = true;
      } else {
        scroll = false;
      }
    });

    RO.observe(component.parentNode);
  });

  onDestroy(() => {
    RO.disconnect();
  });
</script>

<style>
  .containerScroll {
    box-shadow: var(--shadow);
  }
  .container {
    width: 100%;
    overflow-y: hidden;
    box-sizing: border-box;
    display: flex;
  }
  .subcontainer {
    padding-right: var(--scrollPadding);
    overflow-y: auto;
    flex: 1;
    scrollbar-color: var(--scrollColor);
    scrollbar-width: thin;
  }
  .subcontainer::-webkit-scrollbar {
    width: var(--scrollWidth);
    background: transparent;
  }
  .subcontainer::-webkit-scrollbar-track {
    background: 'transparent';
  }
  .subcontainer::-webkit-scrollbar-thumb {
    background: var(--scrollColor);
    border-radius: 5px;
    overflow: hidden;
  }
  .subcontainer::-webkit-scrollbar-thumb:hover {
    background: var(--scrollColorHover);
  }
</style>

<div
  aria-label="container-scroll"
  style="{style}--scrollColor:{scrollColor};--shadow:{shadow};--scrollPadding:{scrollPadding};--scrollWidth:{scrollWidth};--scrollColorHover:{scrollColorHover}"
  class={`container ${scroll ? 'containerScroll' : ''}`}>
  <div
    aria-label="subcontainer-scroll"
    bind:this={component}
    class="subcontainer"
    style={styleSubcontainer}>
    <slot />
  </div>
</div>
