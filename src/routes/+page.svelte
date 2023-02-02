<script>
	let name = '';
</script>



<h1>Welcome {name} !</h1>
<div>Your Name: 
	<input bind:value={name} type="text" placeholder="Text Here...">
	<br><br>
	<i>hoping this web is useful for education</i>
</div>



<style>
	h1 {
		text-align: center;
		color: blueviolet;
	}
	div {
		text-align: center;
	}
</style>
