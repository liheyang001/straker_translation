<template>
    <div>
        <Header></Header>
        <user></user>    
        <Footer></Footer>
    </div>


</template>

<script>
    import User from './components/User.vue';
    import Header from './components/Header.vue';

    import Footer from './components/Footer.vue';

    export default {
        components: {
            Header,
            User,
            Footer
        },
        
    }
</script>

<style>
body{
    background-color: white;
}
</style>
