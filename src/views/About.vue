<template>
    <div class="container">
        <div class="h-cont">
            <div class="top-cont">
                <img src="../assets/img/logo.png"/>
                <p class="t-money">500万元~20万元</p>
            </div>
            <ul>
                <li>
                    <span>额度范围</span>
                    <p>500万元~20万元</p>
                </li>
                <li>
                    <span>额度范围</span>
                    <p>500万元~20万元</p>
                </li>
                <li>
                    <span>年化利率</span>
                    <p>0.59%起</p>
                </li>
            </ul>
        </div>
        <div class="auth">
            <h3>所需授权</h3>
            <ul>
                <li><img src="../assets/img/auth1.png"/></li>
                <li><img src="../assets/img/auth1.png"/></li>
                <li><img src="../assets/img/auth1.png"/></li>
                <li><img src="../assets/img/auth1.png"/></li>
            </ul>
        </div>
        <div class="auth">
            <h3>申请条件</h3>
            <ul class="condition">
                <li>年满18周岁</li>
                <li>持有中国居民身份证的中国大陆公民</li>
            </ul>
        </div>
        <div class="auth">
            <h3>还款方式</h3>
            <ul class="condition">
                <li>从绑定的银行卡中自动扣款</li>
            </ul>
        </div>
        <div class="tab-cont">
            <ul class="t-menu">
                <li @click="checkTab(1)"><a :class="{active:isAnswer}">借款问答</a></li>
                <li @click="checkTab(2)"><a :class="{active:isEvaluate}">用户评价</a></li>
                <li @click="checkTab(3)"><a :class="{active:isIntroduce}">机构介绍</a></li>
            </ul>
            <div class="t-cont" v-if="isAnswer">
                <ul>
                    <li>
                        <h5>· 上征信吗</h5><br/>若借款人逾期不还，逾期账单会影响您的芝麻分和运营商的信用分，进而影响您的个人征信
                    </li>
                    <li>
                        <h5>· 上征信吗</h5><br/>若借款人逾期不还，逾期账单会影响您的芝麻分和运营商的信用分，进而影响您的个人征信
                    </li>
                    <li>
                        <h5>· 上征信吗</h5><br/>若借款人逾期不还，逾期账单会影响您的芝麻分和运营商的信用分，进而影响您的个人征信
                    </li>
                </ul>
            </div>
            <div class="t-cont" v-if="isEvaluate">
                <ul>
                    <li>18684765750 额度挺高的啊 1527834544</li>
                    <li>18684765750 额度挺高的啊 1527834544</li>
                    <li>18684765750 额度挺高的啊 1527834544</li>
                </ul>
            </div>
            <div class="t-cont" v-if="isIntroduce">
                <ul>
                    <img src=""/>
                    <li>
                        玖富集团历经十多年发展，业已形成以移动互联网、大数据科技、生态链发展模块为基础，以消费分期、网络借贷、移动海外证券、大数据评估等为核心业务的综合布局。旗下品牌包括玖富普惠、玖富万卡、悟空理财、玖富金融（原玖富钱包）、蜡笔分期、玖富证券等。目前玖富集团旗下品牌注册用户已经突破5000万。
                    </li>
                </ul>
            </div>
        </div>
        <div class="bottom-button">
            <p>马上拿钱</p>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                isAnswer:true,
                isEvaluate:false,
                isIntroduce:false,
            }
        },
        methods:{
            checkTab(param){
                switch (param){
                    case 1:
                        this.isAnswer = true;
                        this.isEvaluate = false;
                        this.isIntroduce = false;
                        break;
                    case 2:
                        this.isEvaluate = true;
                        this.isAnswer = false;
                        this.isIntroduce = false;
                        break;
                    case 3:
                        this.isIntroduce = true;
                        this.isAnswer = false;
                        this.isEvaluate = false;
                        break;
                    default:
                }
            }
        },
        created(){
        },
    }
</script>
<style lang="scss" scoped>
    .container {
        width: 100%;
        height: 100vh;
    }

    ul li {
        list-style: none;
    }

    .h-cont {
        padding: 20px 10px;
        background: linear-gradient(to bottom, #3a4a5a 50%, #fafafa 50%);
        .top-cont {
            display: flex;
            flex-direction: row;
            background-color: #ffffff;
            border-radius: 10px 10px 0 0;
            padding-bottom: 30px;
            .t-money {
                font-size: 36px;
                color: #3a4a5a;
                margin-left: 10px;
                font-weight: bold;
                margin-top: 25px;
            }
        }
        ul {
            background-color: #ffffff;
            border-radius: 0px 0px 10px 10px;
            box-shadow: 0px 10px 5px #e7e7e7;
            display: flex;
            padding-bottom: 25px;
            li {
                flex-direction: column;
                padding-left: 15px;
                padding-right: 10px;
                border-right: 1px solid #e2e2e2;
                &:last-child {
                    border: none;
                }
                span {
                    font-size: 12px;
                    color: #999;
                }
                p {
                    margin: 0;
                    font-size: 16px;
                    color: #01cf99;
                    font-weight: 500
                }
            }
        }
        img {
            width: 52px;
            height: 52px;
            margin-top: 20px;
            margin-left: 15px;
        }

    }

    .auth {
        h3 {
            padding: 35px 0 0 20px;
            font-weight: normal;
        }
        ul {
            display: flex;
            flex-direction: row;
            li {
                padding-top: 25px;
                padding-left: 15px;
                img {
                    width: 83px;
                    height: 93px;
                }
            }
        }
        .condition {
            display: flex;
            flex-direction: column;
            padding-left: 10px;
            li {
                color: #afafaf;
                font-size: 14px;
                list-style: disc;
            }
        }
    }

    .tab-cont {
        margin-top:50px;
        margin-bottom:90px;
        .t-menu {
            display: flex;
            flex-direction: row;
            li {
                padding-left:30px;
                a {
                    color: #afafaf;
                    font-size: 15px;
                    text-decoration: none;
                }
                .active{
                    color:#01cf99;
                }
            }
        }
        .t-cont{
            h5{
                color:black;
                padding-top:10px;
            }
            padding-top:20px;
            padding-left:20px;
            font-size:16px;
            color: #a0a0a0;
        }
    }
    .bottom-button{
        position: fixed;
        bottom:0;
        left:20px;
        background-color:#3a4a5a;
        border-radius: 10px;
        width:380px;
        height:50px;
        line-height:50px;
        p{
            color:#fff;
            font-size:19px;
            text-align: center;
        }
    }
</style>