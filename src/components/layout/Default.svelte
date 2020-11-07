<script>
    // TODO: add all the required file to make the 
    
    import Navbar from './../../UI/Navbar.svelte'
</script>
<div>
    <Navbar label="GoodCook"/>    
<div class="page-header" data-parallax="true" style="background-image: url('https://images.unsplash.com/photo-1604503279541-7b274b8f7c36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2434&q=80'); transform: translate3d(0px, 115.333px, 0px);">
        <div class="container">
      <div class="row">
        <div class="col-md-8 ml-auto mr-auto">
          <div class="brand">
            <h1>Goood
              <span class="pro-badge">
                Cook
              </span>
            </h1>
            <h3 class="title">Share Great Food with Friends </h3>
          </div>
        </div>
      </div>
    </div>
    </div>
    <div class="main main-raised">
        <slot></slot>
    </div>
</div>