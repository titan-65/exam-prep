<script>
  let recipesFront = [
    {
      id: 1,
      title: 'Frenct Toast',
      category: 'Breakfast',
      preview:
        'Ipsum fugiat labore et elit veniam magna elit Lorem proident excepteur aliqua et id aliquip.',
      image:
        'https://images.unsplash.com/photo-1519340333755-56e9c1d04579?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
      description:
        'Commodo sunt esse sint aliquip enim proident in eu eu sunt non. Commodo in ipsum irure veniam exercitation nostrud deserunt veniam deserunt proident amet. Velit et sit reprehenderit non ad do ipsum reprehenderit ea non ad velit enim. Irure anim deserunt quis duis quis aliquip velit dolore sint culpa est laborum Lorem. Duis dolor enim Lorem nulla officia ipsum adipisicing pariatur et aliquip ut dolor officia culpa. Magna culpa fugiat reprehenderit non adipisicing qui enim exercitation reprehenderit ut occaecat velit.',
    },
    {
      id: 2,
      title: 'Frenct Toast',
      category: 'Breakfast',
      preview: 'Dolor velit irure laborum cillum ex deserunt pariatur non culpa sint.',
      image:
        'https://images.unsplash.com/photo-1557925923-cd4648e211a0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=933&q=80',
      description:
        'Cillum nostrud dolore consequat voluptate in et eiusmod fugiat adipisicing adipisicing. Et est ea enim pariatur eiusmod. Quis enim amet Lorem tempor Lorem cillum velit dolor do Lorem enim labore sunt laborum. Laboris esse quis consectetur ut ullamco. Aute aliqua cillum mollit culpa adipisicing. Sit ut quis Lorem minim labore culpa consectetur nostrud cupidatat incididunt incididunt fugiat enim consequat.',
    },
    {
      id: 3,
      title: 'Frenct Toast',
      category: 'Breakfast',
      preview: 'Dolor velit irure laborum cillum ex deserunt pariatur non culpa sint.',
      image:
        'https://images.unsplash.com/photo-1485474187873-a541e1da7c51?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80',
      description:
        'Cillum nostrud dolore consequat voluptate in et eiusmod fugiat adipisicing adipisicing. Et est ea enim pariatur eiusmod. Quis enim amet Lorem tempor Lorem cillum velit dolor do Lorem enim labore sunt laborum. Laboris esse quis consectetur ut ullamco. Aute aliqua cillum mollit culpa adipisicing. Sit ut quis Lorem minim labore culpa consectetur nostrud cupidatat incididunt incididunt fugiat enim consequat.',
    },
  ]
</script>

<main>
  <section class="section text-center">
    <div class="container">
      <div class="row">
        <div class="col-md-8 ml-auto mr-auto">
          <h2 class="title">Home</h2>
          <h5 class="description">
            We think good food comes from good cooks and we want you to show us you are a
            good cook.
          </h5>
        </div>
      </div>
    </div>
  </section>
  <section class="section">
    <div class="container">
      <h2 class="section-title">Latest Recipes</h2>
      <div class="row">
        {#each recipesFront as recipe}
          <div class="col-md-4">
            <div class="card card-blog">
              <div class="card-header card-header-image">
                <a href="#pablo"> <img src={recipe.image} alt="" /> </a>
                <div
                  class="colored-shadow"
                  style="background-image: url({recipe.image}); opacity: 1;" />
              </div>
              <div class="card-body">
                <h6 class="card-category text-rose">{recipe.category}</h6>
                <h4 class="card-title"><a href="#pablo">{recipe.preview}</a></h4>
                <p class="card-description">{recipe.description}</p>
              </div>
            </div>
          </div>
        {/each}
      </div>
    </div>
  </section>
  <section
    class="section"
    style="background-image: url('https://images.unsplash.com/photo-1604503279541-7b274b8f7c36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2434&q=80')">
    <div class="row">
      <div class="col-md-8 ml-auto mr-auto">
        <h2 class="title">Share</h2>
        <h5 class="title">
          Et tempor in est velit magna non esse sunt. Nostrud fugiat eiusmod tempor sit
          laboris cillum exercitation laboris commodo elit enim reprehenderit exercitation
          anim. Incididunt dolore officia et non ipsum anim aliqua deserunt. Enim quis
          amet reprehenderit dolor magna non cillum dolore sint est cillum proident.
        </h5>
      </div>
    </div>
  </section>
</main>
