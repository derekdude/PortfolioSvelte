<script lang="ts">
  import cn from 'classnames';
  import LinkBorder from './LinkBorder.svelte';

  export let title = 'Title';
  export let value = 'coding';
  export let selected = 'coding';

  function setSelected(value: string) {
    selected = value;
  }
</script>

<button
  class="bordered-link group flex h-auto w-full
  flex-col items-start justify-center md:items-start"
  on:click={() => setSelected(value)}
>
  <LinkBorder />
  <span
    class={cn(
      'font-comfortaa transform self-center py-4 text-xl group-hover:animate-pulse lg:text-3xl',
      { 'text-gray-400': selected === value },
    )}
    >{title}
  </span>
  <LinkBorder />
</button>
