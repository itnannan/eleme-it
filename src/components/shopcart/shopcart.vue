<template>
    <div class="shopcart">
        <div class="content">
            <div class="content-left">
                <div class="logo-wrapper">
                    <div class="logo">
                        <i class="iconfont icon-gouwuche"></i>
                    </div>
                    <div class="num"></div>
                   
                </div>
                 <div class="price">{{deliveryPrice}}元</div>
                 <div class="desc">另需配送费{{deliveryPrice}}</div>
            </div>
            <div class="content-right">
                <div class="pay">￥{{minPrice}}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
          name: 'shopcart',
          props :{
              deliveryPrice :{
                  type :Number,
                  default :0
              },
              minPrice :{
                  type: Number,
                  default :0
              }
          }
    }

</script>

<style scoped lang="stylus"> 
        .shopcart
            position:fixed
            left:0
            bottom:0
            z-index:50
            width:100%
            height:48px
        .content
            display:flex
            background: #141d27
            font-size:0
            .content-left
                flex:1
                .logo-wrapper
                    display:inline-block
                    position:relative
                    top:-10px
                    margin:0 12px
                    padding:6px
                    width:56px
                    height:56px
                    box-sizing:border-box
                    vertical-align:top
                    border-radius:50%
                    text-align:center
                    background: #141d27
                    .logo
                        width:100%
                        height:100%
                        border-radius:50%
                        background:#2b343c
                        .icon-gouwuche
                            line-height:44px
                            font-size:24px
                            color:#80858a
                .price
                    display:inline-block
                    vertical-align:top
                    margin-top:12px
                    line-height:24px
                    padding-right:12px
                    box-sizing:border-box
                    border-right:1px solid rgba(255,255,255,0.1)
                    font-size:16px
                    font-weight:700
                    color:rgba(255,255,255,0.4)
                .desc
                    display:inline-block
                    vertical-align:top
                    margin:12px 0 0 12px
                    line-height:24px
                    font-size:16px
                    color:rgba(255,255,255,0.4)
            .content-right
                flex:0 0 105px
                width:105px
                .pay
                    font-size:12px
                    height:48px
                    line-height:48px
                    text-align:center
                    font-weight:700
                    background:#2b333b
                    color:rgba(255,255,255,0.4)
</style>
