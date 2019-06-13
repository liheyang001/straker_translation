<template>

    <div class="container">
        <ul class="invisible">{{userId}}  </ul>
        <ul v-for="(post, index) in posts">
            <table class="table table-hover">
                <thead class="postThead">
                    <!-- show post if click button -->
                    <tr v-if = "post.userId == userId">
                        <th>UserID</th>
                        <td>{{post.userId}}</td>
                    </tr>
                    <tr v-if = "post.userId == userId">
                        
                        <th>ID</th>
                        <td>{{post.id}}</td>
                    </tr>
                    <tr v-if = "post.userId == userId">
                        <th>Title</th>
                        <!-- show post detail after click post title -->
                        <a name= "post" v-on:click="showBody = true, postID = index">{{post.title}}</a>
                    </tr>
                    <tr v-if = "index == postID">
                        <th v-if = "showBody">Body</th>
                        <td v-if = "showBody">{{post.body}}</td>
                        
                    </tr>
                </thead>
            </table>
        </ul>
          
    </div>

</template>

<script>
    var postURL = 'https://jsonplaceholder.typicode.com/posts';
    export default {
        props: ['userId'],
        data: function(){
                return {
                    showBody : false,
                    postID: -1
                    }
            },
            mounted(){
                fetch(postURL)
                .then(response => response.json())
                .then((data) => {
                    this.posts = data;
                    });
            },
            methods: {

            }
            
    }
</script>

<style>
a {
    display: block;
    text-align: center;
}
</style>

