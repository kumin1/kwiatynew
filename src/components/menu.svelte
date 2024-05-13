<script>
    import { onMount } from 'svelte';
    import { location, push } from 'svelte-spa-router';

    let menuOpen = false;

    function revealMenu(event) {
        event.stopPropagation();
        const menuIcon = document.getElementById('menu-open');
        const closeIcon = document.getElementById('menu-close');
        const menudropdown = document.querySelector('.menu-dropdown');
        const menu = document.getElementById('menu');

        if (menuOpen) {
            menuIcon.style.display = 'block';
            closeIcon.style.display = 'none';
            menudropdown.style.display = 'none';
            menu.style.backgroundColor = '';

            menu.style.zIndex = '3';
        } else {
            menuIcon.style.display = 'none';
            closeIcon.style.display = 'block';
            menudropdown.style.display = 'flex';
            menu.style.backgroundColor = 'var(--maincolor)';
        }

        menuOpen = !menuOpen;
    }

    function handleClickOutside(event) {
        const menudropdown = document.querySelector('.menu-dropdown');
        if (menuOpen && !menudropdown.contains(event.target)) {
            revealMenu(event);
        }
    }

    onMount(() => {
        document.addEventListener('click', handleClickOutside);
        return () => {
            document.removeEventListener('click', handleClickOutside);
        };
    });
</script>

<div class="menu" id="menu">
    <div class="menu-container container">
        <div class="home-link">
            <a>Placeholder</a>
        </div>
        <div class="site-links">
            <a>Produkty</a>
            <a>O nas</a>
            <a>Kontakt</a>
            <a>Galeria</a>
        </div>
        <div class="menu-dropdown-icons">
            <button on:click={revealMenu}>
                <img src="./images/menu-open.png" id="menu-open">
                <img src="./images/menu-close.png" id="menu-close">
            </button>
        </div>
    </div>
</div>
<div class="menu-dropdown">
    <a on:click={()=> {push('/produkty')}} >Produkty</a>
    <a on:click={()=> {push('/produkty')}} >Produkty</a>
    <a on:click={()=> {push('/produkty')}} >Produkty</a>
    <a on:click={()=> {push('/produkty')}} >Produkty</a>
    <a on:click={()=> {push('/produkty')}} >Produkty</a>
</div>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400..700&family=Madimi+One&family=Mali:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;1,200;1,300;1,400;1,500;1,600;1,700&family=Manrope:wght@200..800&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap');
    #menu-open{
        display: block;
    }
    #menu-close{
        display: none;
    }
    .menu-dropdown{
        display: none;
        flex-direction: column;
        text-align: center;
        background-color: var(--maincolor);
        padding-bottom: 15px;
        gap: 0.75rem;
        position: absolute;
        top: 100px;
        width: 100%;
        z-index: 3;
    }
    .menu-dropdown a{
        color: var(--textwhite);
        font-weight: 500;
        font-size: 1.75rem;
        font-family: "Poppins", sans-serif;
        text-shadow: 0 4px 4px #00000040;
        text-decoration: none;
        z-index: 3;
    }

    .home-link{
        margin-top: auto;
        margin-bottom: auto;
        margin-left: 1rem;
        font-family: "Nanum Pen Script", cursive;
        font-size: 3.25rem;
        font-weight: 500;
        z-index: 3;
    }
    .menu-dropdown-icons{
        margin-top: auto;
        margin-bottom: auto;
        z-index: 3;
    }
    .menu-dropdown-icons button{
        background-color: inherit;
        border: none;

    }
    .menu-dropdown-icons img{
        width: 50px;
        height: 50px;
    }
    .site-links{
        display: none;
        gap: 1rem;
        margin-right: 1rem;
    }
    .site-links a{
        font-family: "Poppins", sans-serif;
        text-shadow: 0 4px 4px #00000040;
        font-size: 1.50rem;
        z-index: 3;
    }
    .menu{
        width: 100%;
        z-index: 2;
        position: relative;
    }
    .menu-container{
        display: flex;
        justify-content: space-between;
        padding: 1rem;
    }
    .menu-container a{
        color: var(--textwhite);
        text-decoration: none;
    }
    .container {
        width: 100%;
        margin-left: auto;
        margin-right: auto;
        padding-left: 0.5rem;
        padding-right: 0.5rem;
    }

    /* xs */
    @media (min-width: 475px) {
        .container {
            max-width: 475px;
        }
    }

    /* sm */
    @media (min-width: 640px) {
        .container {
            max-width: 640px;
        }
    }

    /* md */
    @media (min-width: 768px) {
        .container {
            max-width: 768px;
        }
        .menu-dropdown-icons{
            display: none;
        }
        .site-links{
            display: flex;
            margin-top: auto;
            margin-bottom: auto;
        }
    }

    /* lg */
    @media (min-width: 1024px) {
        .container {
            max-width: 1024px;
        }
    }

    /* xl */
    @media (min-width: 1280px) {
        .container {
            max-width: 1280px;
        }
    }

    /* 2xl */
    @media (min-width: 1536px) {
        .container {
            max-width: 1536px;
        }
    }

</style>