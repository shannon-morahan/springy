<script>
    import * as d3 from "d3"
	export let name;

    const url = window.location;
    const urlObject = new URL(url);
    const json = urlObject.searchParams.get('json')

</script>

<style>
	h1 {
		color: green;
	}
</style>

<div id="my_dataviz"></div>

<h1>Hello There dd {JSON.stringify(json)}!</h1>
