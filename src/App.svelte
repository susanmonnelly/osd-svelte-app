<script lang="ts">
	import { onMount } from 'svelte';
  import OpenSeadragon from "openseadragon";
  let viewer = {};

  onMount( () => {
    viewer = OpenSeadragon({
          id: 'osd',
          prefixUrl: '/openseadragon/images/',
          animationTime: 0.5,
          blendTime: 0.1,
          constrainDuringPan: true,
          maxZoomPixelRatio: 2,
          minZoomLevel: 1,
          visibilityRatio: 1,
          zoomPerScroll: 2,
          tileSources:
            '/openseadragon/beck.dzi',
        }) ;
	});
</script>

<style>
  .osd {
      height: 100%;
      width: 100%;
  }
</style>

  <h1>Beck</h1>
  <div
    class="osd"
    id="osd"
  ></div>
