<script lang="ts">
  export let gradient: string[] = ["#FDFFEE", "#8BDCFF"];
  export let title: string = "";
  export let backsplashImage: string = "";
  export let long: boolean = false;

  /**
   * 0: Min degree for backsplash rotation
   * 1: Max degree for backsplash rotation
   */
  const DEGREE_CONSTRAINTS = [-10, 10];

  // rotation de
  let rotationDegree = Math.random() * (
    DEGREE_CONSTRAINTS[1] - DEGREE_CONSTRAINTS[0]
  ) + DEGREE_CONSTRAINTS[0];

  /**
   * Spaces some given text with one space between each character
   * @param text - the text to modify
   */
  export function spaceLetters(text: string) {
    let acc: string = "";
    for (let i = 0; i < text.length; i++) {
      acc += `${text[i]} `;
    }

    return acc;
  }

  let text:HTMLElement;
</script>
<div class={`sticky ${long && "long"}`}>
  <div class="content" style={`background-image:linear-gradient(${gradient?.toString()})`}>
    {#if title}
      <h2>{spaceLetters(title)}</h2>
    {/if}
    <p bind:this={text}>
      <slot/>
    </p>
  </div>
  <div class="backsplash" style={`
    ${backsplashImage ? `background-image: url('${backsplashImage}');` : ""};
    transform: rotate(${rotationDegree}deg)`}
  >
  </div>
</div>

<style>
  .sticky {
    position: relative;
    margin: 1em;
    width: 100%;
  }

  .sticky.long .content {
    padding-bottom: min(50vh, 8em);
  }

  .sticky .content {
    box-shadow: 0 4px 4px #00000025;
    padding: 1em;
    padding-bottom: 3em;
  }

  .sticky .content h2 {
    font-family: 'Bebas Neue', sans-serif;
    font-weight: normal;
    text-transform: uppercase;
    font-size: 50px;
    margin: 0;
  }

  .backsplash {
    background-color: red;
    position: absolute;
    height: 100%;
    width: 100%;
    top: 0;
    transform: rotate(358deg);
    z-index: -1;
    background-size: 50px;
  }
</style>