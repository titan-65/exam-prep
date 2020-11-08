<script>
    // TODO: Add the necessary feature to web app
    // TODO: Create form for addition of new Recipes (CRUD)
    // TODO: Setup Contenful

    import Feedbar from '.././UI/Feedbar.svelte'
    import Modal from './Recipes.svelte'

    let recipeTitle;
    let description;
    let preview;
    let image;
    let category;
    let newsFeedRecipes = []

    $: modal = false

    function modalTrigger(event) {
        modal = true;
        enterValue = event.target.value
    }

    function closeModal() {
        modal = false;
    }

    function onFormSubmit() {
        // TODO: Validate form on submit

        newsFeedRecipes = [
            ...newsFeedRecipes,
            {
                id: new Date().toISOString(),
                title: recipeTitle,
                desc: description,
                prev: preview,
                cate: category,
                img: image
            }
        ]
    }
</script>
<div class="section">
    <!-- <h1 class="title">GooodCook Recipes</h1> -->
    <section class="section">
        <div class="container">
            <Feedbar />
            <section class="section">
                  <div class="container card">
                      <p class="title text-cemter">Share your new recipe</p>
                      <form>
                          <span class="bmd-form-group">
                                <div class="input-group">
                                    <input type="text" class="form-control" bind:value="{recipeTitle}"  placeholder="Type your new recipe">
                                </div>
                          </span>
                          <div class="row">
                                <div>
                                    <button class="btn btn-primary" on:click|preventDefault="{modalTrigger}" data-toggle="modal" data-target="#myModal">Add Recipe</button>
                                </div>
                          </div>
                      </form>
                  </div>
                  <div class="row">
                      {#each newsFeedRecipes as recipe}
                        <div class="col-md-4">
                          <div class="card card-blog">
                            <div class="card-header card-header-image">
                              <a href="#pablo"> <img src={recipe.img} alt="" /> </a>
                              <div
                                class="colored-shadow"
                                style="background-image: url({recipe.img}); opacity: 1;" />
                            </div>
                            <div class="card-body">
                              <h6 class="card-category text-rose">{recipe.cate}</h6>
                              <h4 class="card-title"><a href="#pablo">{recipe.prev}</a></h4>
                              <p class="card-description">{recipe.desc}</p>
                            </div>
                          </div>
                        </div>
                      {/each}
                    </div>

            </section>
        </div>
        <!-- Sidebar -->
        <!-- <div class="sidebar ps" data-background-color="black" >
        <div class="sidebar-wrapper ps">
            <ul class="nav">
                <li class="nav-item">
                    <a class="nav-link" href="#">
                        <i class="material-icons">dashboard</i>
                    </a>
                </li>
            </ul>

        </div>
        <div class=".sidebar sidebar-background" style="background-image: url('https://images.unsplash.com/photo-1565004602745-718e1b0d44f8?ixlib=rb-1.2.1&auto=format&fit=crop&w=1290&q=80');">

            </div>
        </div> -->
    </section>
    {#if modal}
        <div class="modal fade" id="myModal" tabindex="-1" role="dialog" style="display: none;" aria-hidden="true">
            <div class="modal-dialog" role="document">
              <div class="modal-content">
                <div class="modal-header">
                  <h5 class="modal-title">Modal title</h5>
                  <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <i class="material-icons">clear</i>
                  </button>
                </div>
                <div class="modal-body">
                  <form>
                        <div class="form-group bmd-form-group">
                            <input type="text" class="form-control" bind:value="{recipeTitle}" placeholder="title">
                          </div>
                          <div class="form-group bmd-form-group">
                              <input type="text" class="form-control" bind:value="{description}" placeholder="description">
                            </div>
                            <div class="form-group bmd-form-group">
                                <input type="text" class="form-control" bind:value="{preview}" placeholder="preview">
                              </div>
                              <div class="form-group bmd-form-group">
                                  <input type="text" class="form-control" bind:value="{image}" placeholder="image">
                                </div>
                            <div class="form-group bmd-form-group">
                                  <input type="text" class="form-control" bind:value="{category}" placeholder="image">
                                </div>
                    </form>
                </div>
                <div class="modal-footer">
                  <button type="button" class="btn btn-link" on:click|preventDefault="{onFormSubmit}">Submit</button>
                  <button type="button" class="btn btn-danger btn-link" data-dismiss="modal">Close<div class="ripple-container"><div class="ripple-decorator ripple-on ripple-out" style="left: 31.0781px; top: 18px; background-color: rgb(244, 67, 54); transform: scale(8.50976);"></div></div></button>
                </div>
              </div>
            </div>
          </div>
    {/if}

</div>

<style>

    .sidebar {
        position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        z-index: 2;
        width: 260px;
        box-shadow: 0 16px 38px -12px rgba(0, 0, 0, 0.56), 0 4px 25px 0 rgba(0, 0, 0, 0.12), 0 8px 10px -5px rgba(0, 0, 0, 0.2);
    }
    .sidebar .sidebar-wrapper {
        position: relative;
        height: calc(100vh - 75px);
        overflow: auto;
        width: 260px;
        z-index: 4;
        padding-bottom: 30px;
    }
    .sidebar .sidebar-background {
        position: absolute;
        z-index: 1;
        height: 100%;
        width: 100%;
        display: block;
        top: 0;
        left: 0;
        background-size: cover;
        background-position: 50%;
    }
    .sidebar[data-background-color=black] {
        background: #191919;
    }
</style>