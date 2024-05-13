<script>

</script>
<div class="top-img">
    <img src="./images/placeholder.jpg">
</div>
<div class="recommended">
    <header>Jakis tekst</header>
    <p>Jakis tekst maly</p>
    <div class="recommended-items">
        <div class="recommended-item">
            <img src="./images/placeholder.jpg">
        </div>
        <div class="recommended-item">
            <img src="./images/placeholder.jpg">
        </div>
        <div class="recommended-item">
            <img src="./images/placeholder.jpg">
        </div>
    </div>
</div>
<!--<div class="newest-products">-->
<!--    <header class="newest-header">Najnowsze Produkty</header>-->
<!--    <div class="newest-items">-->
<!--        <div class="product">-->
<!--            <div class="product-image">-->
<!--                <div class="arrow-left">-->
<!--                    <img src="./images/left-arrow.png">-->
<!--                </div>-->
<!--                <img src="./images/placeholder.jpg">-->
<!--                <div class="arrow-right">-->
<!--                    <img src="./images/right-arrow.png">-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="product-name">-->
<!--                <header>Nazwa obrazu</header>-->
<!--            </div>-->
<!--            <div class="product-price">-->
<!--                <p>cena - 100zł</p>-->
<!--            </div>-->
<!--        </div>-->
<!--    </div>-->
<!--</div>-->
<style>
    @import url('https://fonts.googleapis.com/css2?family=Jacques+Francois&family=Raleway:ital,wght@0,100..900;1,100..900&family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap');

    .product-name header{
        color: var(--textwhite);
        font-family: "Ubuntu", sans-serif;
        font-size: 3rem;
    }
    .product-price{
        color: var(--textwhite);
        font-family: "Raleway", sans-serif;
        font-size: 1.5rem;
    }
    .newest-products{
        display: flex;
        flex-direction: column;
        text-align: center;
    }
    .newest-header{
        font-family: "Jacques Francois", serif;
        font-size: 2rem;
        color: var(--textwhite);
    }
    .newest-items{
        display: flex;
        flex-wrap: wrap;
    }
    .product{
        min-width: 25%;
        margin-left: auto;
        margin-right: auto;
    }
    .product-image{
        position: relative;
        display: flex;
    }
    .product-image img{
        width: 100%;
    }
    .arrow-left{
        position: absolute;
        top: 50%;
        left: 10px;
        transform: translateY(-50%);
    }
    .arrow-left img{
        width: 12px;
        height: 25px;
    }
    .arrow-right{
        position: absolute;
        top: 50%;
        right: 10px;
        transform: translateY(-50%);
    }
    .arrow-right img{
        width: 12px;
        height: 25px;
    }

    .top-img{
        width: 100%;
        height: 500px;
        position: relative;
        top: -110px;
    }
    .top-img img{
        width: 100%;
        height: 500px;
        object-fit: cover;
    }
    .recommended{
        display: flex;
        flex-direction: column;
        text-align: center;
        color: var(--textwhite);
        position: relative;
        top: -20px;
    }
    .recommended header{
        font-size: 4rem;
        font-family: "Jacques Francois", serif;
    }
    .recommended p{
        font-family: "Nanum Pen Script", cursive;
        font-size: 2.5rem;
        margin-bottom: 30px;
    }
    .recommended-items{
        display: flex;
        flex: 0 0 33.33%;
        flex-wrap: wrap;
    }
    .recommended-item{
        min-width: 33.33%;
        padding: 10px;
        margin-left: auto;
        margin-right: auto;
    }
    .recommended-item img{
        width: 100%;
    }
    @media screen and (min-width: 768px) {
        .recommended-items {
            flex-wrap: nowrap; /* Prevent wrapping */
        }
        .recommended-item {
            flex: 0 0 33.33%; /* Set width to 33.33% for three items on a line */
        }
    }
</style>