
<script lang="ts">
  import Numbers from './Numbers.svelte';

  let count: number = 0
  $: doubled = count *2

  const increment = () => {
    count += 1
  }
</script>

<button on:click={increment} > 
 Clicked  { count } { count === 1 ? 'time' : 'times'}
</button>

<p> {count} doubled is {doubled} </p>

<Numbers/>

<Numbers marks={[count]}/>