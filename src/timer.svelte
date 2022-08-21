<script>
Notification.requestPermission();
let hours = 0;
let minutes = 0;
let seconds = 0;
let totalNumber = 0;
let result = "your not done";

$: ahours = hours * 3600000;
$: aminutes = minutes * 60000;
$: aseconds = seconds * 1000; 
function done(){
    console.log("done")
    result = "you are done";
    new Notification("Yo its done dude")
}

function startTimer(){
    result = "you are not done";
setTimeout(done, ahours + aminutes + aseconds);
}
</script>

<main>
    <h1>Timer</h1>
    <!--functionality-->
    <div class="general">
    <div>
    <p>Hours</p>
    <input type="numbers" bind:value={hours}>
    </div>
    <div>
    <p>Minutes</p>
    <input type="numbers" bind:value={minutes}>
    </div>
    <div>
    <p>Seconds</p>
    <input type="numbers" bind:value={seconds}>
    </div>
    </div>
    <button on:click={()=>{startTimer()}}>Start timer</button>
    <div>
    <p>{result}</p>
    </div>
</main>

<style>
    .general{
        display:flex;

    }
</style>