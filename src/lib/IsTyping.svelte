<script>
 let isFocused=false

 function handleFocus(){
    isFocused=true
 }
 function handleBlur(){
    isFocused=false
 }
</script>
 
<main class="w-full h-full flex items-center justify-center">
 <div class="w-96 h-5/6 bg-white rounded-2xl flex flex-col items-center justify-center gap-y-6">
  <input class="border rounded-2xl  h-12 w-5/6 px-2" type="text" on:focus={handleFocus} on:blur={handleBlur} placeholder="username">
  
  <div>
   {#if isFocused===true}
   <div>you are typing ...</div>
   {:else}
   <div>you stopped typing!!</div>
   {/if}
   

  </div>
 </div>
</main>