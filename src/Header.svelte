<script>
  import { Link } from "@c0ldra1n/svero";
</script>

<style>
  /* $pink: #D96C9F;
$lgtpink: #F2AECE;
$purple: #582C59;
$darkpurple: #230F26;
$pinkapricot: #F2BBBB; */

  header {
    display: flex;
    justify-content: space-between;
    height: 10vh;
    background: linear-gradient(to bottom, #582c59 0%, #230f26 100%);
  }

  nav ul {
    display: flex;
    list-style-type: none;
    margin: 0;
  }

  :global(header a) {
    padding: 1em;
    display: block;
    color: white !important;
  }

  :global(.logo) {
    font-weight: bold;
    text-decoration: none;
  }
    :global(.logo):hover {
        color: #F2AECE !important;
        text-decoration: none !important;
    }

  .container {
    width: 70%;
    margin: auto;
    display: flex;
    justify-content: space-between;
  }

li {
    color: #F2AECE;
    font-weight: 500;
    text-decoration: none;
}

</style>

<header>
  <div class="container">
    <Link href="/" className="logo">Developers</Link>
    <nav>
      <ul>
        <li>
          <Link className="logo" href="/">Index</Link>
        </li>
        <li>
          <Link className="logo" href="/about">About</Link>
        </li>
      </ul>
    </nav>
  </div>
</header>
