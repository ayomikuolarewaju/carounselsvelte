<script>
export let data
let images = data.imgs

let no = 0
let revImg = images[no].im

const rev =(id)=>{
  let img = images.filter((img)=>img.id === id)
  revImg = img[0].im
} 


</script>


<div class="container flex flex-col p-10 space-y-5 mx-auto my-auto items-center overflow-hidden">
  <div>
    <img src="{revImg}" alt="" width="800" height="200">
  </div>
  <div class="container flex flex-row mx-auto my-auto ">
    {#each images as img }
    <img src="{img.btn}" alt="" width="20" height="20" on:click={()=>rev(img.id)} on:keydown class = "cursor-pointer overflow-hidden">
    {/each}
    </div>
</div>





