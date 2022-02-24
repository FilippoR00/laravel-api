<template>
    <header>
        <div class="container">
            <div class="left">
                <h1>Boolpress</h1>
            </div>
            <div class="right">
                <a href="admin/home">Area riservata</a>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
}
</script>

<style lang="scss" scoped>
    header{
        background-color: #3535ec;
        height: 100px;
        color: 	white;
        position: sticky;
        top: 0;
        .container{
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            .left{
                h1{
                    font-size: 40px;
                }
            }
            .right{
                a{
                    background-color: #5e5eff;
                    padding: 15px 25px;
                    border-radius: 10px;
                    color: white;
                    text-decoration: none;
                    transition: 0.3s all;
                }
                a:hover{
                    background-color: #6d6dff;
                }
            }
        }
    }
</style>