<script>
  let version = '1.2.0';
  let date = '2024-04-21';

  let linqAverage = [1, 2, 3, 4].average(); //testing linq
  let linqAverageExpected = 2.5;
</script>

<div id="header">
  <span class="block">Cloned from <a href="https://gitlab.com/rgrueneis/svelte4">Svelte4 at gitlab</a></span>
  <span id="version">v{version}</span>
  <span id="author">[rgrueneis, {date}]</span>
</div>

<div>
  Standard svelte 4 project (<i>npm create svelte@latest</i>) with following adaptions:
  <ul>
    <li>Packages and rules for eslint added (version 8)</li>
    <li>Script for eslint added</li>
    <li>SASS support added</li>
    <li>Bootstrap and Bootstrap Icons added</li>
    <li>LINQ polyfill added</li>
    <li>Prepared for SPA generation</li>
  </ul>
</div>

<h3>Testing tools</h3>
<div>
  This button should look like a Bootstrap success button:
  <button class="btn btn-success">Bootstrap success</button>
</div>
<div>
  This button should display the bootstrap trash icon:
  <button type="button" class="btn btn-primary">
    <i class="bi bi-trash"></i>
  </button>
</div>
<div>
  Test linq.polyfill.ts - this value should be {linqAverageExpected}:
  <span class="badge" style:background-color={linqAverage === linqAverageExpected ? 'green' : 'red'}>
    {linqAverage}</span>
</div>

<style lang="scss">
  $version-color: blue;
  #header {
    margin-bottom: 0.5em;
  }
  #version {
    color: $version-color;
  }
  #author {
    font-style: italic;
  }
  .block {
    display: block;
  }
  div {
    margin-bottom: 0.5em;
    padding-bottom: 0.2em;
    &:not(:last-child) {
      border-bottom: 1px solid #eee;
    }
  }
</style>