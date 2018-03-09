<template>
	<div class="banner">
        <ul class="clearfix">
            <li><img src="../assets/images/img_1.jpg" alt=""/>
            	<div class="text-box">
                	<h2>冰雪奇观11111</h2>
                    <p>图片11 / 文</p>
                </div>
            </li>
            <li><img src="../assets/images/img_2.jpg" alt=""/>
            	<div class="text-box">
                	<h2>海中奇石</h2>
                    <p>图片22 / 文</p>
                </div>
            </li>
            <li><img src="../assets/images/img_3.jpg" alt=""/>
            	<div class="text-box">
                	<h2>湖光奇色333</h2>
                    <p>图片33 / 文</p>
                </div>
            </li>
            <li><img src="../assets/images/img_4.jpg" alt=""/>
            	<div class="text-box">
                	<h2>山谷奇景44444</h2>
                    <p>图片44 / 文</p>
                </div>
            </li>
        </ul>
        <ol>
            <li class="active"></li>
            <li></li>
            <li></li>
            <li></li>
        </ol>
    </div>
</template>
<script>
	export default {
		mounted(){
			this.fnSlider();
		},
		watch:{
			// '$route':function(){
			// 	alert(1);
			// }
		},
		methods:{
			fnSlider(){
				$(function (){
					var mySwipe=new Swipe($('.banner')[0],{
						auto:2000,
						continuous:true,
						stopPropation:true,
						callback:function (index,element){
							$('.banner ol li').removeClass('active');
							$('.banner ol li').eq(index).addClass('active');
						}
					});
				});
			}
		}
	}
</script>