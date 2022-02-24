<template>
    <main>
        <div class="container">
            <h2>Lista post:</h2>
            <ul>
                <li v-for="post in posts" :key="post.id">
                    <div class="card">
                        <img v-if="post.image" :src="'./././storage/' + post.image" :alt="post.title + ' image'">
                        <img v-if="!post.image" src="https://www.penworthy.com/Image/Getimage?id=C:\Repositories\Common\About%20Us\Slide1.jpg" alt="no image">
                        <h3>{{post.title}}</h3>
                    </div>
                </li>
            </ul>
        </div>
    </main>
</template>

<script>
export default {
    name: "Main",
    data() {
        return {
            posts: []
        }
    },
    created() {
        axios.get('/api/posts')
            .then( (response) => {
                this.posts = response.data;
            })
    },
}
</script>

<style lang="scss" scoped>
    main{
        .container{
            h2{
                margin: 50px 25px;
            }
            ul{
                display: flex;
                justify-content: center;
                flex-wrap: wrap;
                gap: 50px;
                li{
                    cursor: pointer;
                    list-style: none;
                    width: calc(100% / 2 - 50px);
                    .card{
                        img{
                            width: 100%;
                            margin-bottom: 20px;
                        }
                        height: 700px;
                        background-color: #e3e7f0;
                        padding: 30px;
                    }
                }
            }
        }
    }
</style>