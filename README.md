<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <title>3D正方体</title>
  	<style type="text/css">
		body{
			background:#000;
		}
		nav{
			width:500px;
			height:500px;
			display:flex;
			-webkit-transform-style: preserve-3d;
					transform-style: preserve-3d;
			position:relative;
			top:300px;
			left:600px;
			perspective:50000px;
			animation:change 32s linear infinite alternate;
/*			transform:rotateX(89deg);*/
		}
		nav:hover{
			animation-play-state:paused;
		}
		@keyframes change{
			form{}
			50%{
				transform:rotateX(360deg) rotateY(180deg) rotateZ(180deg);
			}
			96%{
				transform:rotateX(360deg) rotateY(360deg) rotateZ(360deg);
			}
			to{
				transform:rotateX(360deg) rotateY(360deg) rotateZ(360deg);
			}
		}
		div{
			width:500px;
			height:500px;
			position:absolute;
			top:0;
			left:0;
			opacity:0.5;
		}
		.before{
			background:#0f0;
			background-size:cover;
			transform:translateZ(250px);
		}
		.later{
			background:#00f;
			background-size:cover;
			transform:translateZ(-250px) rotateX(180deg);
		}
		.left{
			background:#f00;
			background-size:cover;
			transform:translate(-250px) rotateY(90deg);
		}
		.right{
			background:#ff0;
			background-size:cover;
			transform:translate(250px) rotateY(-90deg);
		}
		.top{
			background:#f0f;
			background-size:cover; 
			transform:translateY(250px) rotateX(90deg);
		}
		.bottom{
			background:#0ff;
			background-size:cover;
			transform:translateY(-250px) rotateX(-90deg);
		}
	</style>
 </head>
 <body>
	<nav>
		<div class="before"></div>
		<div class="later"></div>
		<div class="left"></div>
		<div class="right"></div>
		<div class="top"></div>
		<div class="bottom"></div>
	</nav>
 </body>
</html>
