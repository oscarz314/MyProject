<script>
	import TodoList from "./Todolist.svelte";
	import Timer from "./timer.svelte";
	import Calculator from "./calc.svelte";
</script>

<!--main intro-->
<div>
<h1 class="MainHeading">Hello Introductions</h1>
<p>I've built websites before in school in school in 6th and 8th grade using replit and other tools.
	But this is really the first one I've built just for myself and to showcase my own still upons creating and things using a javascript framework.
	Below I will be building cools things. 
</p>
</div>
<!-- styles for intro-->
<style>
	.MainHeading{
		text-align: center;
	}
</style>

<!--Rest-->
<div>
<TodoList/>
<Timer/>
<Calculator/>
</div>