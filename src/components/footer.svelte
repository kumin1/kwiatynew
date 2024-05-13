<script>

</script>

<div class="footer">
    <div class="footer-item">
        <header>Produkty</header>
        <div class="footer-links">
            <a class="footer-items">Kwiaty</a>
<!--            <img src="./images/text-between.png">-->
            <a class="footer-items">Jakis produkt</a>
<!--            <img src="./images/text-between.png">-->
            <a>Jakis produkt</a>
        </div>
    </div>
    <div class="footer-item">
        <header>Obserwuj nas</header>
        <div class="footer-links">
            <a class="footer-items">Facebook</a>
<!--            <img src="./images/text-between.png">-->
            <a class="footer-items">Instagram</a>
<!--            <img src="./images/text-between.png">-->
            <a>Pinterest</a>
        </div>
    </div>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap');
    .footer{
        display: flex;
        justify-content: space-around;
        gap: 3rem;
        flex-wrap: wrap;
        padding-top: 100px;
        padding-bottom: 100px;
    }
    .footer-item{
        text-align: center;
    }
    .footer-links a {
        color: var(--textlight);
        font-family: "Ubuntu", sans-serif;
        font-size: 1.2rem;
        position: relative;
        margin-left: 3px;
        margin-right: 3px;
    }

    .footer-links a:nth-child(n+2)::after {
        content: '';
        position: absolute;
        top: 5px;
        left: -6px;
        height: 20px;
        width: 2px;
        background-color: var(--textlight);
    }
    .footer-item > * {
        min-width: fit-content;
        flex: 1;
    }
    .footer-item header{
        font-weight: 500;
        color: var(--textdark);
        font-size: 1.5rem;
    }

</style>