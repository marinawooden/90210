<script lang="ts">
  export let src: string;
  export let alt: string;
</script>

<div
  style={`background-image:url(${src})`}
  role="img"
  aria-label={alt}
>
</div>

<style>
  div {
    height: 100px;
    width: 100%;
    background-position: center;
    background-size: 100% auto;
    box-shadow: 0 4px 4px #00000025;
  }
</style>
