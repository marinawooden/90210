<script lang="ts">
  export function spaceLetters(text: string) {
    let acc: string = "";
    for (let i = 0; i < text.length; i++) {
      acc += `${text[i]} `;
    }

    return acc;
  }
</script>
<div id="logo">
  <div id="image-logo">
    <img src="./img/logo.png" id="show-logo"/>
    <img src="./img/cast 1.png" />
  </div>
  <div id="text-logo">
    <h1>90210</h1>
    <h2>{spaceLetters("Beverly Hills")}</h2>
  </div>
</div>

<style>
  #logo {
    width: 263px;
    height: 261px;
    position: relative;
    margin-bottom: 30px;
    margin: 0 auto;
    margin-top: 50px;
  }

  #image-logo {
    display: flex;
    justify-content: center;
  }

  #image-logo img:not(:last-of-type){
    position: absolute;
    z-index: -1;
  }

  #show-logo {
    width: 175px;
    height: 175px;
    animation: spin 5s linear infinite;
    transform-origin: center;
  }

  h1, h2 {
    font-family: 'SF Hollywood Hills', 'Impact', sans-serif;
  }

  h2 {
    text-transform: uppercase;
  }

  h1, h1::before {
    font-size: 100px;
    background: linear-gradient(#fff 49%, #000 50%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    margin: 0;
  }

  h1::before {
    content: "90210";
    text-shadow: 0 4px 10px #00000050;
    position: absolute;
    z-index: -1;
  }

  #text-logo {
    text-align: center;
    position: absolute;
    bottom: 0px;
    left: 12px;
  }

  #text-logo > * {
    margin: 10px;
  }

  @keyframes spin {
    0% {
      transform: rotate(0deg);
    }

    100% {
      transform: rotate(360deg);
    }
  }
</style>