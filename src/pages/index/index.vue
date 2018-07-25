<template>
    <div>
        <h2>JS </h2>
        <ul v-for="list in jscomponents"
            v-bind:key="list.title">
            <li v-on:click="changeNav(list)"><a>{{list.title}}</a></li>
        </ul>

    </div>
</template>

<script>
export default {
    data:function(){
        return {
            jscomponents:[
                {
                    title:'JS布局-AJAX获取数据瀑布流布局',
                    link:'waterfall.html'
                },
                {
                    title:'JS布局-木桶布局',
                    link:'barrels.html'
                },
                {
                    title:'JS组件-面向对象-轮播图(带缩略图)',
                    link:'carousel.html'
                },
                {
                    title:'JS组件-面向对象-曝光加载',
                    link:'exposure.html'
                },
                {
                    title:'JS组件-面向对象-tab切换',
                    link:'switchtab.html'
                }
            ]
        }
    },
    methods:{
        changeNav:function(e){
            location.href=`${e.link}`
        }

    }  
}
</script>

<style>
	  a{
			color:#333;;
			text-decoration:none;
		}
		
		a:hover{
			color:green;
		}
		
        ul,li{
            list-style:none;
        }
		
		li{
			font-family:"Monaco";
            cursor:pointer;
		}
</style>


