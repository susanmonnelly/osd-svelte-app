<script>
export let onChange;
let selected;
$: onChange(selected)
</script>

<style>
  .toc {
      width: 25%;
      height: 5%;
      -ms-flex-align: start;
  }

</style>

 <div class="toc">

	<select bind:value={selected} on:change="{() => console.log(selected)}">
    <option value="Ben">Ben</option>
    <option value="Megi">Megi</option>
    <option value="Beck">Beck</option>
  </select>

 </div>
