<script lang="ts">
	import OSD from "./library/OSD.svelte"
  import TOC from "./library/TOC.svelte"

 let selectValue = ''
</script>

<TOC onChange={newValue => selectValue = newValue} />
  <p>Toc box value is: {selectValue}</p>
<OSD tocValue={selectValue}/>


