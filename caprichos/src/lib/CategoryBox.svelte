<script>
    export let title = "";
    export let foods = [];
</script>

<div class="container">
    <div class="title-bar">
        <h2>{title}</h2>
    </div>
    <div class="table-food">
        {#each foods as food}
                <div>
                    <b>{food.name}</b>
                    <p>{food.description}</p>
                </div>
                <div class="line">
                    <h3>C$ {food.price}</h3>
                </div>
        {/each}
        </div>
</div>

<style>
    .container {
        box-sizing: border-box;
        display: flex;
        width: 100%;
        padding-top: 50px;
        padding-left: 60px;
        position: relative;
        flex-direction: column;
    }
    .title-bar {
        height: 50px;
        width: 100%;
    }
    .title-bar::before {
        content: "";
        position: absolute;
        width: 60%;
        background-color: #fbcea3;
        height: 20px;
        margin-top: 17px;
    }
    .title-bar h2 {
        position: relative;
        z-index: 2;
        padding-left: 4px;
    }
    .line {
        border-left: 4px solid #fd5211;
        padding-left: 4px;
    }
    .table-food{
        display: grid;
        grid-template-columns: 1fr 100px;
        font-size: 0.8rem;
    }
    .table-food > div{
        padding: 5px;
        margin: 8px 0px;
        display: grid;
        align-content: center;
    }
    .table-food > div > p{
        color: #686868;
    }
</style>
