<script lang="ts">
let count =$state(parseInt(JSON.parse(localStorage.getItem("count")||"0")));
 function handleClick(action:string){
  if(action==="--"){
    if(count<=0){
      return alert("count can't be less then 0")
    }
    count --
  }else{
    count ++
  }
 }
 $effect(()=>{
  localStorage.setItem("count", count.toString());
 })
</script>

<main class="bg-slate-700 w-screen h-screen flex items-center justify-center">
  <div class="w-96 h-96 bg-white rounded-2xl shadow-2xl flex flex-col gap-y-8 items-center justify-center ">
  <div class="bg-slate-200 w-60 h-18 rounded-full text-center flex items-center justify-center text-2xl font-bold">
    Count:{count}
  </div>
  <div class="flex gap-4 text-2xl font-bold">
    <button on:click={()=>handleClick("++")} class="px-6 cursor-pointer shadow-md bg-yellow-600 py-4 text-center flex items-center justify-center rounded-full">+</button>
    <button on:click={()=>handleClick("--")} class="px-6 cursor-pointer shadow-md bg-green-600 py-4 text-center flex items-center justify-center rounded-full">-</button>
  </div>
  </div>
</main>

