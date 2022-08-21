<script>
  let vOne = 0;
  let vTwo = 0;
  let done = 0;


</script>
<main>
    <div>
        <h1>Calculator</h1>
        <p>*enter values first before calculation</p>
        <div class="who">
        <input type="numbers" bind:value={vOne}> <input type="numbers" bind:value={vTwo}> <p> = {done}</p>
        </div>
        <div class="buttons"> 
        <button on:click={()=>{done=vOne+vTwo}}>+</button>
        <button on:click={()=>{done=vOne-vTwo}}>-</button>
        <button on:click={()=>{done=vOne*vTwo}}>x</button>
        <button on:click={()=>{done=vOne/vTwo}}>/</button>
        <button on:click={()=>{console.log(done)}}>=</button>

        </div>
    </div>



</main>
<style>
    .who{
        display:flex
    }
    .who > p{
        font-size:20px;
    }
</style>