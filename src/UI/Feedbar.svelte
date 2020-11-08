<script>
  // your script goes here
  import { links } from 'svelte-routing'
</script>
<nav class="navbar navbar-expand-lg bg-dark">
  <div class="container">
    <div class="navbar-translate" use:links>
      <a href="/recipes" class="navbar-brand">
          Recipes
          
        </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="sr-only">Toggle navigation</span>
        <span class="navbar-toggler-icon" />
        <span class="navbar-toggler-icon" />
        <span class="navbar-toggler-icon" />
      </button>
    </div>
    <div class="collapse navbar-collapse">
      <ul class="navbar-nav">
        <li class="active nav-item">
            <a href="#pablo" class="nav-link">
                <span class="material-icons">
            home
        </span>
    </a></li>
        <li class="nav-item"><a href="#pablo" class="nav-link">
            <span class="material-icons">
            dashboard
        </span>
        </a></li>
        <li class="dropdown nav-item">
          <a
            href="#pablo"
            class="dropdown-toggle nav-link"
            data-toggle="dropdown">Dropdown</a>
          <div class="dropdown-menu">
            <h6 class="dropdown-header">Dropdown header</h6>
            <a href="#pablo" class="dropdown-item">Action</a>
            <a href="#pablo" class="dropdown-item">Another action</a>
            <a href="#pablo" class="dropdown-item">Something else here</a>
            <div class="dropdown-divider" />
            <a href="#pablo" class="dropdown-item">Separated link</a>
            <div class="dropdown-divider" />
            <a href="#pablo" class="dropdown-item">One more separated link</a>
          </div>
        </li>
      </ul>
    </div>
  </div>
</nav>
