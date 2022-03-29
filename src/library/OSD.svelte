<script lang="ts">
  import { onMount } from 'svelte';
  import OpenSeadragon from "openseadragon";
  let viewer = {};
  export let tocValue = '';
  let dogName = 'Megi'


function renderViewer(tileSource) {
  console.log(tileSource)
  viewer = OpenSeadragon({
      id: 'osd',
      prefixUrl: '/openseadragon/images/',
      tileSources: '/openseadragon/' + tileSource + '.dzi',
    });
}

  onMount( () => {
    renderViewer(dogName);
  });


</script>

<style>
  .osd {
      height: 100%;
      width: 80%;
      -ms-flex-align: end;
  }
</style>

  <p>tilesource is: {'/openseadragon/' + tocValue + '.dzi'}</p>

  <div
    class="osd"
    id="osd"
  ></div>

