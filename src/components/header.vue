<template>
    <header class="header" :class="{'is-bg':bg,'is-fixed':fixed}">
        <div class="headerRutern is-left">
            <slot name="left"></slot>
        </div>
        
        <h1 class="header-title" v-text="title"></h1>
        
        <div class="headerRutern is-right">
            <slot name="right"></slot>
        </div>
        
        
    </header>
</template>
<script>
   export default{
    props:{
        title:{
            type:String,
            default:''
        },
        bg:{
            type:Boolean,
            default:false
        },
        fixed:{
            type:Boolean,
            default:false
        }
    }
   }
</script>
<style lang="scss">
.header{
    display: flex;
    align-items: center;
    height: 0.8rem;
    padding: 0 0.1rem;
    background: #fff;
    color:rgb(73,73,73);
    border-bottom:1px solid #eee;
    a{
        display: inline-block;
        color:rgb(73,73,73);
    }
    .headerRutern{
        width: 0.7rem;
        align-items:stretch;
        &.is-left{
            text-align: left;
        }
        &.is-right{
            text-align: right;
        }
        .icon-img{
            width: 0.36rem;
            height: 0.36rem;
        }
        .margin-right-10{
            margin-right: 0.1rem;
        }
    }
    .header-title{
        flex: 1;
        text-align: center;
        font-size: 0.36rem;
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow: hidden;
    }
    &.is-bg{
        background:#ff0000;
        color: #fff;
        a{
          color: #fff;
        }
        .header-title{
            color: #fff;
        }
    }
    &.is-fixed{
        position: fixed;
        left: 0;
        right: 0;
        top: 0;
        z-index: 9;
    }
}
</style>