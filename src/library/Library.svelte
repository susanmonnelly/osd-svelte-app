<script>
  import { OpenSeadragon } from "openseadragon";
  OpenSeadragon({
      id: 'openSeaDragon',
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
    })
</script>
<style>
  .viewer {
      width: 100%;
      height: 100%;
      background-color: #434343;
  }
</style>


<div class="viewer" id="openSeaDragon"></div>
