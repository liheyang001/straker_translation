

<template>

    <div class="{activeclass:isShow}" id="user-data">
        <div class="container">
            
            <ul v-for="(user, index) in users">
                <!-- show user detail button and show user post button -->
                <button @click = 'userToShow = index' class="btn btn-primary btn-sm">Show User Details</button>
                <button @click = 'postToShow(user.id)' class="btn btn-primary btn-sm">Show User Posts</button>
                <table class="table table-hover">
                    <thead>
                    
                        <tr>
                            <th>ID</th>
                            <td>{{user.id}}</td>
                        </tr>
                        <tr>
                            <th>Name</th>
                            <td>{{user.name}}</td>    
                        </tr>
                        <!-- show user info after click button -->
                        <tr v-show = "userToShow == index">
                            <th>Username</th>
                            <td>{{user.username}}</td>
                        </tr>
                        <tr v-show = "userToShow == index">
                            <th>Email</th>
                            <td>{{user.email}}</td>
                        </tr>
                        <tr v-show = "userToShow == index">
                            <th>Street</th>
                            <td>{{user.address.street}}</td>
                        </tr>
                        <tr v-show = "userToShow == index">
                            <th>Suite</th>
                            <td>{{user.address.suite}}</td>
                        </tr>
                        <tr v-show = "userToShow == index">
                            <th>City</th>
                            <td>{{user.address.city}}</td>
                        </tr>                           
                        <tr v-show = "userToShow == index">
                            <th>ZipCode</th>
                            <td>{{user.address.zipcode}}</td>
                        </tr>
                        <tr v-show = "userToShow == index">
                            <th>Geo lat</th>
                            <td>{{user.address.geo.lat}}</td>
                        </tr>     
                        <tr v-show = "userToShow == index">
                            <th>Geo lng</th>
                            <td>{{user.address.geo.lng}}</td>
                        </tr>  
                        <tr v-show = "userToShow == index">
                            <th>Phone</th>
                            <td>{{user.phone}}</td>
                        </tr>  
                        <tr v-show = "userToShow == index">
                            <th>Website</th>
                            <td>{{user.website}}</td>
                        </tr>  
                        <tr v-show = "userToShow == index">
                            <th>Company Name</th>
                            <td>{{user.company.name}}</td>
                        </tr>  
                        <tr v-show = "userToShow == index">
                            <th>CatchPhaser</th>
                            <td>{{user.company.catchPhrase}}</td>
                        </tr>  
                        <tr v-show = "userToShow == index">
                            <th>BS</th>
                            <td>{{user.company.bs}}</td>
                        </tr>  

                    </thead>
                    
                </table>


            </ul>
            
        <post :userId="userID"></post>    
        </div>
                
    </div>

</template>

<script>
    import Post from './Post.vue';
    var userURL = 'https://jsonplaceholder.typicode.com/users';


export default {

    data: function(){
            return {
                users:[],
                userToShow: -1,
                ID: -1,
                userID: -1
                }
        },
        mounted(){
            fetch(userURL)
            .then(response => response.json())
            .then((data) => {
                this.users = data;
                });
        },
        methods: {
            postToShow: function(ID){
                this.userID = ID;

            }
        },
        components:{
            Post
        }

}
</script>

<style>
 #user-data{
    padding-top: 10rem;
} 

tr > th {
    width: 200px;
}
tr > td {
    text-align:center;
}
</style>
