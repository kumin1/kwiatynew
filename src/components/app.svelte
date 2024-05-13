<script>
    import Router from "svelte-spa-router";
    import Index from "./index.svelte";
    import Menu from "./menu.svelte";
    import Footer from "./footer.svelte";
    import Produkty from "./produkty.svelte";
    import Onas from "./onas.svelte";
    import Kontakt from "./kontakt.svelte";
    import Galeria from "./galeria.svelte";


    let strony = {
        '/': Index,
        '/produkty': Produkty,
        '/onas': Onas,
        '/kontakt': Kontakt,
        '/galeria': Galeria,
    };
</script>

<main>
    <Menu />
    <Router routes={strony} />
    <Footer />
</main>

<style>
    main {
        width: 100%;
        height: 100%;
        margin: 0;
        padding: 0;
        background-color: var(--maincolor);
    }
    :root{
        --maincolor: #CFCFC1;
        --textwhite: #FFFFFF;
        --textlight: #AAA697;
        --textdark: #848073;
        --textblack: #000000;
    }
</style>

