<script>
  import Sticky from "../components/sticky.svelte";
  import NavBar from "../components/navbar.svelte";
  import Logo from "../components/logo.svelte";
  import SplashImg from "../components/splashimg.svelte";
  import Poll from "../components/poll.svelte";
</script>

<Logo />
<NavBar />
<main>
  <div class="col">
    <Sticky
      backsplashImage="./img/butterfly.jpeg"
      title="Welcome"
    >
      <p>
        This is a place to talk about
        the original run of 90210, airing from 1990-2000.  I haven't
        been able to find that many active pages about the show- so
        I'm going to try to stay dedicated.
      </p>
    </Sticky>
    <Sticky
      gradient={["#FFE9AF", "#FF9C64"]}
      long={true}
      backsplashImage="./img/flowers.gif"
    >
      <h3>
        Updates
      </h3>
      <p>
        This show has not been on the air for almost a 1/4 century so
        I don't think there'll be any updates
      </p>
    </Sticky>
  </div>
  <div class="col">
    <Sticky
      gradient={["#FFE1F5", "#EFC0FF"]}
      backsplashImage="./img/checker.png"
      long={true}
    >
      <SplashImg
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-bb_L3pTUF3mGB3ZwGFxsEkIWFJCUcs-hpFJSN5kx1QDBjLa2O2vKXbpPg2LNJTaX2Cg&usqp=CAU"
        alt="the hollywood sign"
      />
      <h2>Poll</h2>
      <Poll topic="characters" />
    </Sticky>
    <Sticky
      backsplashImage="./img/sunflower.jpeg"
    >
      <p>
        
      </p>
    </Sticky>
  </div>
</main>
<footer>
  <p>
    <small>c. 2023 Marina Wooden.  I just wanted to make something with Svelte</small>
  </p>
</footer>


<style>
  main {
    width: 100%;
    max-width: 800px;
    margin: 0 auto;
    display:flex;
    gap: 10px;
  }

  main img {
    width: 100%;
    box-shadow: 0 4px 4px #00000025;
  }

  .col {
    width: 50%;
  }

  footer {
    position: sticky;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 20px;
    top: 100vh;
    bottom: 0;
  }

  footer p {
    margin: 0;
  }
</style>