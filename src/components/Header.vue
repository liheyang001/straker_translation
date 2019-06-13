<template>
    <!-- header link -->
    <header class="main-header">
            <!-- logo -->
            <div>
                <a href="https://www.straker.co.nz/" class="main-header__brand">
                    <img src="../assets/logo.png" alt="straker - your translation agent">
                </a>
            </div><nav class="main-nav">
                <ul class="main-nav__items">
                    <li class="main-nav__item">
                        <!-- back to top -->
                        <a href="#">User Details</a>
                    </li>
                    <li class="main-nav__item">
                        <!-- to the post -->
                        <a href="#post">User Posts</a>
                    </li>
                </ul>
            </nav>
    </header>
</template>

<script>
export default {
    
}
</script>

<style>
.main-header {
    width: 100%;
    position: fixed;
    background: lightgreen;
    padding: 0.5rem 1rem;
    top :0px;
    left: 0;
    z-index: 1;
    height:7rem;
}

.main-header > div {
    display: inline-block;
    vertical-align: middle;
}

.main-header__brand{
    color: #0e4f1f;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.4rem;
    height: 1.4rem;  
    display: inline-block;
}

.main-nav{
    display: inline-block;
    text-align: right;
    width:calc(100% - 80px);
    vertical-align: middle;
}

.main-nav__items {
    margin:0;
    padding: 0;
    list-style:none;
}

.main-nav__item{
    display: inline-block;
    margin: 0 1rem;
}

.main-nav__item a{
    text-decoration: none;
    color: #000;
    font-weight: bold;
    padding: 3px 0;
}


.main-nav__item a:hover,
.main-nav__item a:active
{
    color: white;
    border-bottom: 5px solid white;
}

.main-header__brand img {
    height:6rem;
}


</style>
