<script>
  import { Router, Route } from 'svelte-routing';
  import DemoMY from './pages/DemoMY.svelte';
  import Home from './pages/Home.svelte';
  import PartnerDemoMY from './pages/PartnerDemoMY.svelte';
  import ProductDetail from './pages/ProductDetail.svelte';

  export let url = '';
  const { env } = process;
  const basepath = env.BASE_PATH;
</script>

<main>
  <Router {url} {basepath}>
    <Route path="/" component={DemoMY} />
    <Route path="home" component={Home} />
    <Route path="partner" component={PartnerDemoMY} />
    <Route path="detail" component={ProductDetail} />
  </Router>
</main>
