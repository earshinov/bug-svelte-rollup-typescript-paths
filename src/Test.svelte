<script>
  import { Route, Router } from 'svelte-navigator';

  import Demos from './routes/Demos.svelte';
  import Home from './routes/Home.svelte';
  import NotFound from './routes/NotFound.svelte';
  import Pts from './routes/Pts.svelte';
  import NavLink from './ui/NavLink.svelte';
</script>

<Router>
  <nav>
    <NavLink to="pts">PTS</NavLink> |
    <NavLink to="demos">Component demos</NavLink>
  </nav>
  <div>
    <Route path="/" component={Home} />
    <Route path="pts" component={Pts} />
    <Route path="demos/*" component={Demos} />
    <Route component={NotFound} />
  </div>
</Router>

<style lang="scss">
  @use '../style/variables' as vars;

  nav {
    margin-bottom: vars.$unit * 2;
  }
</style>
