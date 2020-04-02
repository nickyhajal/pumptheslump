<script>
  export let segment;
</script>

<style lang="scss">
  @import "../style/theme";
  nav {
    display: grid;
    grid-template: "logo links" auto / auto auto;
    justify-content: space-between;
    background: $main-color;
    font-weight: 300;
    padding: 0 1em;
    color: $white;
    font-weight: bold;
    font-size: 1.7rem;
    place-items: center;
    a {
      color: $white;
    }
  }

  ul {
    grid-area: links;
    margin: 0;
    padding: 0;
  }

  /* clearfix */
  ul::after {
    content: "";
    display: block;
    clear: both;
  }

  li {
    display: block;
    float: left;

    a {
      font-size: 1rem;
    }
  }

  [aria-current] {
    position: relative;
    display: inline-block;
  }

  [aria-current]::after {
    position: absolute;
    content: "";
    width: calc(100% - 1em);
    height: 2px;
    display: block;
    bottom: -1px;
  }

  #logo {
    display: block;
    grid-area: logo;
  }
  a {
    text-decoration: none;
    padding: 1em 0.5em;
    display: block;
  }
</style>

<nav>
  <a href="/" id="logo">#PumpTheSlump</a>
  <ul>
    <li>
      <a
        aria-current={segment === 'contribute' ? 'page' : undefined}
        href="/contribute">
        Find a Job
      </a>
    </li>

    <!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
    <li>
      <a
        rel="prefetch"
        aria-current={segment === 'blog' ? 'page' : undefined}
        href="blog" />
    </li>
  </ul>
</nav>
