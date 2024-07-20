<script>
    let code = '';
    let productName = '';
    let playerCount = 0;
    let productAlreadyExists = false;

    let products = [];
    let createNewProduct = (productName) => {
        if (!products.includes(productName)) {
            productAlreadyExists = false;
            products = [...products, productName]; // Add product if it doesn't exist
        } else {
            productAlreadyExists = true;
            console.log(`${productName} already exists.`);
        }
    };

    function createNewGame() {
        code = Math.random().toString(36).substring(2, 15);

    }

</script>

<div class="container-fluid">
    <h1>Admin</h1>

    {#if productAlreadyExists}
        <p style="background: red">{productName} already exists.</p>
    {/if}

    <input on:input={productAlreadyExists = false} bind:value={productName} type="text" placeholder="Product Name">
    <button on:click={createNewProduct(productName)}>Add</button>

    <table>
        <tr>
            <th>Products</th>
        </tr>
        {#each products as product}
            <tr>
                <td>{product}</td>
            </tr>
        {/each}
    </table>

    <input bind:value={playerCount} type="number" placeholder="Player Count">

    <button on:click={createNewGame()}>New Game</button>

    <div>{code}</div>
</div>