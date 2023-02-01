<script>
    let teksInput = '';
	let tdList = [];
	function addList(){
		tdList = [...tdList, {text: teksInput}];
	}
    function elimi(index){
        tdList.splice(index, 1);
        tdList = tdList;
    }
</script>



<h1>YOUR LIST !!!</h1>
<div class="inputSection">Add List: 
	<input bind:value={teksInput} type="text" placeholder="Text Here...">
	<button type="button" on:click={addList}>add</button>
</div>

<div class="listSection">
    {#each tdList as item, index}
	<span>{index + 1},{item.text}<button on:click={() => elimi(index)}>xXx</button></span><br>
    {/each}
</div>

<style>
    h1 {
        margin: 0 auto;
        text-align: center;
        font-family: 'Courier New', Courier, monospace;
    }
    div.inputSection {
        margin: 0 auto;
        color: darkcyan;
        text-align: center;
    }
    div.listSection {
        margin-left: 30%;
        text-align: left;
    }
</style>
