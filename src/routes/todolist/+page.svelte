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

<h1>Your List !</h1>
<div class="inputSection">Add List: 
    <input maxlength='50' bind:value={teksInput} type="text" placeholder="Text Here...">
    <button type="button" on:click={addList}>add</button>
</div>
<h3>List kamu:</h3>
<div class="listSection">
    <a>
    {#each tdList as item, index}
        <span class="daftarList"> {index+1}. {item.text}
        <span class="delList" on:click={() => elimi(index)}>delete</span></span>
    {/each}
    </a>
</div>
    
<style>
    h1 {
		text-align: center;
		color: blueviolet;
        padding: 4px 6px 4px 6px;
        border: 1px solid #091540;
        margin-left: 20%;
        margin-right: 20%;
	}
    h3 {
		text-align: center;
		color: blueviolet;
        padding: 4px 6px 4px 6px;
        border: 1px solid #091540;
        margin-left: 20%;
        margin-right: 20%;
	}
    span.daftarList {
        padding: 12px 4px 12px 4px;
        background-color: aquamarine;
        position: relative;
        display: block;
        margin-top: 1px;
    }
    span.delList {
        font-weight: bold;
        cursor: pointer;
        position: absolute;
        right: 0;
        top: 0;
        padding: 12px;
        background-color: aqua;
        color: crimson;
    }
    span.delList:hover{
        background-color: blue;
        color: aliceblue;
    }
    div.inputSection {
        margin: 0 auto;
        color: darkcyan;
        text-align: center;
    }
    div.listSection {
        padding-top: 20px;
        padding-bottom: 20px;
        margin-left: 20%;
        text-align: left;
        margin-right: 20%;
    }
</style>    
    