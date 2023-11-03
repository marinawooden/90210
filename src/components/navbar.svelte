<nav>
  <a href=".">About the Show</a>
  <a href=".">Where to Watch</a>
  <a href=".">Articles</a>
  <a href=".">Quizzes</a>
  <a href=".">Shoutbox</a>
</nav>

<style>
  a {
    text-decoration: none;
    color: black;
    transition: 0.3s ease color;
  }

  a:hover {
    color: white;
  }

  a:hover::after {
    color: black;
  }

  nav {
    font-family: 'Khmer MN', serif;
    text-transform: uppercase;
    text-align: center;
    margin: 3em;
  }

  nav a:not(:last-of-type)::after {
    content: " ︱";
  }
</style>