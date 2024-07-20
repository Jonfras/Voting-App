<script>
    import Button from 'bootstrap/js/src/button.js';
    import {goto} from '$app/navigation';

    let code = '';

    function navigateTo(uri) {
        return () => {
            goto(uri);
        };
    }
</script>

<div class="container-fluid">
    <h1>Voting-App</h1>
    <button on:click={navigateTo('admin')}>Admin</button>

    <input bind:value={code} type="text" placeholder="Code">
    <button on:click={navigateTo(`vote/${code}`)}>Vote</button>
</div>

<style>

</style>
