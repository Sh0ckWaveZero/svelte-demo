<script lang="ts">
  import { Button } from 'flowbite-svelte'

  let count: number = 0
  const increment = () => {
    count += 1
  }

  const decrement = () => {
    count -= 1
  }
</script>

<p class='mb-3'>{count}</p>

<Button class="!bg-green-500"on:click={increment}>count + </Button>
<Button class="!bg-yellow-500"on:click={decrement}>decrement -</Button>
