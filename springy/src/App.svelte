<script>
    import * as d3 from "d3"

import { onMount } from 'svelte';

	onMount(() => {
		var editor = ace.edit("editor");
        editor.setTheme("ace/theme/monokai");
        editor.session.setMode("ace/mode/json");

        const url = window.location;
        const urlObject = new URL(url);
        const json = urlObject.searchParams.get('json');
        editor.getSession().setTabSize(2);
        editor.getSession().setUseWrapMode(true);

        // const fJsonString = JSON.stringify(json, null, '\t');

        editor.setValue(json);
        // editor.setValue(json);
	});

	export let name;



</script>

<style>
	h1 {
		color: green;
	}

    #editor {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
    }

</style>

<div id="editor">function foo(items)


</div>


