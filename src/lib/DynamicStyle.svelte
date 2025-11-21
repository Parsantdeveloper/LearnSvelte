<script>

 let light=$state(false)
</script>

<main class="bg-black w-screen h-screen" class:light={light}>
 <div class="w-screen h-12 flex items-center justify-end px-40">
  <button on:click={()=>light=!light}  class="bg-white px-2 py-2 rounded-2xl shadow cursor-pointer">
    {#if light===false}
    Turn on Light
    {:else}
    Turn Off Light
    {/if}
</button>
 </div>
 
</main>

<style>
  .light{
    background-color: white;
  }
</style>