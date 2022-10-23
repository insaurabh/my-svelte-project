<script lang="ts">

  export let marks: number[] = [1,2,3];

  const addNumber =  () => {
    marks = [...marks, marks.length + 1];
   } 

   $: sum = marks.reduce((t,n) => t + n, 0)
</script>

<p>{marks.join(' + ')} =  {sum}</p>

<button on:click={addNumber}>
    Add a number
</button>

{#if sum === 5} 
 { alert(sum) }
{/if}