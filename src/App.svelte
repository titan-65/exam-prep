<script>
  import { Router, Link, Route } from 'svelte-routing'
  import Recipes from './routes/Recipes.svelte'
  import Home from './routes/Home.svelte'
  import Default from './components/layout/Default.svelte'

  export let url = ''
</script>

<style>
</style>

<Router url="{url}">
	<Default>
	  <Route path="recipes" component="{Recipes}" />
	  <Route path="/"><Home/></Route>

</Default>
</Router>

