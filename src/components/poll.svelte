<script lang="ts">
  import pollData from "../lib/data/polldata.json";
  export let topic: string;
</script>

<div>
  <h3>Poll Title</h3>
  <p class="">
    Poll subtitle.  This will include some short splash text
    describing what we're voting for.
  </p>
</div>

<style>
  div {
    background-color: white;
    background-image: linear-gradient(white 60%, rgb(225, 225, 225));
    box-shadow: 0 0 0 1px #00000015, 2px 4px 4px #00000025;
    padding: 1em;
    border-radius: 10px;
  }

  h3, p {
    margin: 0.1em;
  }

  p {
    font-size: 0.7em;
    font-style: italic;
  }
</style>