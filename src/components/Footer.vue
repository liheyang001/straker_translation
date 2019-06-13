<template>
    <!-- footer link -->
    <nav class="main-footer">
        <ul class="main-footer__links">
            <li class="main-footer__link">
                <a href="https://www.straker.co.nz/">Support</a>
            </li>
            <li class="main-footer__link">
                <a href="https://www.straker.co.nz/">Terms of Use</a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    
}
</script>

<style>
    .main-footer {
        background: black;
        padding: 2rem;
        margin-top: 3rem;
    }

    .main-footer__links{
        list-style:none;
        margin:0;
        padding:0;
        text-align: center;
    }

    .main-footer__link {
        display:inline-block;
        margin:0 1rem;
    }

    .main-footer__link a {
        color: white;
        text-decoration: none;
    }

    .main-footer__link a:hover,
    .main-footer__link a:active{
        color: #ccc;
    }
</style>
