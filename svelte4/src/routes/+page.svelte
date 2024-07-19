<script>
  import TestComponent from '$lib/components/TestComponent.svelte';
</script>

<div class="container-fluid">
  <h1>Svelte 4</h1>
  <TestComponent />
</div>

<style lang="scss">
  // next line to make bootstrap incl. icons available in the whole project
  @import 'bootstrap/dist/css/bootstrap.min.css';
  @import 'bootstrap-icons/font/bootstrap-icons.min.css';
</style>
