<script>
  let product = [
    {
     name:"electronics",
     price:2596,
     size:"3xl"
    },
    {
     name:"electronics",
     price:2596,
     size:"3xl"
    },
    {
     name:"electronics",
     price:2596,
     size:"3xl"
    },
    {
     name:"electronics",
     price:2596,
     size:"3xl"
    }
  ]
</script>

<div class="w-full h-full items-center justify-center flex flex-col ">
    {#each product as data}
    <div class="w-96 h-96 bg-amber-50 shadow-inner  flex items-center justify-center flex-col">
      <div>
       <div>
        {data.name}
       </div>
       <div>
        {data.price}
       </div>
    </div>
    <div>
     {data.size}
    </div>
</div>
{/each}
    {#each product as data}
    <div class="w-96 h-96 bg-amber-50 shadow-inner  flex items-center justify-center flex-col">
      <div>
       <div>
        {data.name}
       </div>
       <div>
        {data.price}
       </div>
    </div>
    <div>
     {data.size}
    </div>
</div>
{/each}
</div>

