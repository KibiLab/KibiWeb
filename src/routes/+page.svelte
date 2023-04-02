<script>
  let components = [
    {id:'button', mainStyle:'btn btn-primary', customStyle:'color:red !important', content:"Click me!"}, 
    {id:'div', mainStyle:'px-10 py-10 bg-slate-300', customStyle:'color:red !important', content:"Hello World from div"}
  ];

	function addComponent() {
		components = [...components, {id:'button', mainStyle:'btn btn-primary', customStyle:'color:red !important', content:"Add me!"}];
	}

  export let tempVar;
  export let Warning;
  function checkEmpty() {
    Warning = 'Change fired!'
    
    if(tempVar == ''){
      tempVar = '&nbsp';
    }
	}
 
  $: {
    console.log(tempVar);
  }

</script>
<div class="px-10 py-10">
  <button class="btn btn-primary" on:click={addComponent}>
    Add a component
  </button>
</div>

<h1 class="text-3xl py-8 px-8 font-bold">{tempVar}</h1>

<div class="px-10">
  <ul>
    {#each components as { id, mainStyle, customStyle, content }, i }
      <li>{i+1}: {id} - mainStyle: {mainStyle} - customStyle: {customStyle}</li>
      {#if id == 'button'}
        <button class="{mainStyle}" style="{customStyle}">                   
          <div contenteditable="true" bind:innerHTML={tempVar} on:keypress={checkEmpty}>{content}</div>
        </button>
      {/if}

      {#if id == 'div'}
        <div class="{mainStyle}"  style="{customStyle}" contenteditable="true">
          {content}
        </div>
      {/if}
    {/each}
  </ul>
</div>
<p>{Warning}</p>