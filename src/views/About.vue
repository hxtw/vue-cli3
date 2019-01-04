<template>
    <div class="container">
        <div class="h-cont">
            <div class="top-cont">
                <img src="../assets/img/logo.png"/>
                <p>500万元~20万元</p>
            </div>
            <ul>
                <li>
                    <span>额度范围</span>
                    <i>500万元~20万元</i>
                </li>
                <li>
                    <span>额度范围</span>
                    <i>500万元~20万元</i>
                </li>
                <li>
                    <span>年化利率</span>
                    <i>0.59%起</i>
                </li>
            </ul>
        </div>
        <div class="auth">
            <h3>所需授权</h3>
            <ul>
                <li><img src="../assets/img/logo.png"/></li>
                <li><img src="../assets/img/logo.png"/></li>
                <li><img src="../assets/img/logo.png"/></li>
                <li><img src="../assets/img/logo.png"/></li>
            </ul>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .container {
        width: 100%;
        height: 100vh;
    }

    ul li {
        list-style: none;
    }

    .h-cont {
        padding:20px 10px;
        background: linear-gradient(to bottom, #3a4a5a 50%, #fafafa 50%);
        .top-cont {
            display: flex;
            flex-direction: row;
            background-color:#ffffff;
            border-radius: 20px 20px 0 0;
        }
        ul{
            background-color:#ffffff;
            border-radius: 0 0 20px 20px;
        }
        img {
            width: 82px;
            height: 82px;
        }
        p {
            font-size: 46px;
            color: #3a4a5a;
        }

    }
</style>