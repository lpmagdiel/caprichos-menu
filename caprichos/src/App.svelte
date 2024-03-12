<script>
    import CategoryBox from "./lib/CategoryBox.svelte";
    import foods from "../public/foods.json";
</script>

<main>
    <div class="container-menu-text">
        <h1>Menú</h1>
    </div>
    <header>
        <h2>Caprichos café</h2>
    </header>
    <CategoryBox title="Comida ligera" foods={foods.light}/>
    <CategoryBox title="Comida a la carta" foods={foods.saucers}/>
    <CategoryBox title="Café helado" foods={foods.couldCoffe}/>
    <CategoryBox title="Café helado" foods={foods.drinks}/>
</main>


<style>
    main{
        width: 100%;
        min-height: 100vh;
        display: inline-block;
    }
    .container-menu-text{
        position: absolute;
        font-size: 3rem;
    }
    .container-menu-text h1{
        writing-mode: sideways-lr;
        text-orientation: upright;
        margin-left: -65px;
        font-family: "PTSerif";
        font-weight: bold;
        color: #FD5211;
    }
    main h2{
        text-align: right;
        padding: 10px;
        font-family: "PTSerif";
        text-decoration: underline;
        background-color: #FD5211;
        float: right;
        color: #ffffff;
    }
</style>