<template>
    <footer>
        <div class="container">
            <a href="#">footer links</a>
            <a href="#">footer links</a>
            <a href="#">footer links</a>
            <a href="#">footer links</a>
            <a href="#">footer links</a>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",
}
</script>

<style lang="scss" scoped>
    footer{
        background-color: #3535ec;
        margin-top: 50px;
        height: 100px;
        .container{
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
            a{
                color: white;
                text-decoration: none;
                margin: 0px 20px;
            }
        }
    }
</style>