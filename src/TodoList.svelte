<script>
    let list = [];
    let task = "";

    function addList(){
        list = [...list, task]
        console.log(list);
        task = "";
    }
    function handleDone(){
        
    }
</script>
<main>
    <h1>Todolist</h1>
    <!--list-->
    <ul>
    {#each list as list}
    <li>{list}
    {/each}
    </ul>
    <!--buttons-->
<div>
    <input type="text" bind:value={task}>
<button on:click={()=>{addList()}}>Add</button>
</div>
</main>