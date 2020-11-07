<script>
  // your script goes here
  import { Link, Route } from 'svelte-routing'
  export let label
</script>

<style>
    a {
        color: inherit;
    }
    .anchfix {
        color: inherit;
    }
</style>

<div>
  <nav
    class="navbar navbar-inverse bg-dark fixed-top navbar-expand-lg"
    id="sectionsNav">
    <div class="container">
      <div class="navbar-translate">
          <Link to="/">
        <a class="navbar-brand"> {label} </a>
          </Link>
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
        <ul class="navbar-nav ml-auto">
           
          <li class="dropdown nav-item">
            <!-- svelte-ignore a11y-missing-attribute -->
            <a class="nav-link">
                 <Link to="recipes" class="anchfix">
              <i class="material-icons">view_carousel</i>
              Recipes
                      </Link>

            </a>
          </li>

          <li class="button-container nav-item iframe-extern">
            <a
              href="https://www.creative-tim.com/product/material-kit-pro?ref=presentation"
              target="_blank"
              class="btn  btn-rose   btn-round btn-block">
              <i class="material-icons">shopping_cart</i>
              Buy Now
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</div>

