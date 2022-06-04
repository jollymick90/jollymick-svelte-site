<!-- <script lang="ts">
    import { Router, Link, Route } from 'svelte-routing';
    import LandingMockPage from './pages/LandingMockPage.svelte';
    import PortalMockPage from './pages/PortalMockPage.svelte';
  
    import Tailwind from './Tailwind.svelte';
    export let url = '';
  </script>
  
  
  <main>
    <Router {url}>
      <nav>
        <Link to="/">Home</Link>
        <Link to="landing">Landing</Link>
        <Link to="portal">Portal</Link>
      </nav>
      <div>
        <Route path="portal" component={LandingMockPage} />
        <Route path="landing"><PortalMockPage /></Route>
        <Route path="/">
          <div>ciao</div>
        </Route>
      </div>
    </Router>
  </main>
   -->