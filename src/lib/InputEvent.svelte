<script>
let name=$state("")
let email=$state("")
let password=$state("")

function handleInput(event){
 
}
</script>
 
<main class="w-full h-full flex items-center justify-center">
 <div class="w-96 h-5/6 bg-white rounded-2xl flex flex-col items-center justify-center gap-y-6">
  <input class="border rounded-2xl  h-12 w-5/6 px-2" type="text" bind:value={name} placeholder="username">
  <input class="border rounded-2xl  h-12 w-5/6 px-2" type="text" bind:value={email} placeholder="email">
  <input class="border rounded-2xl  h-12 w-5/6 px-2" type="text" bind:value={password} placeholder="password">
  <button class="w-5/6 bg-yellow-600 py-2 rounded-full text-slate-200 hover:opacity-60 cursor-pointer">Signup</button>
  <div>
    {#if name||email||password}
    <div>name : {name}</div>
     <div>email : {email}</div>
     <div>password : {password}</div>
    {/if}
  </div>
 </div>
</main>