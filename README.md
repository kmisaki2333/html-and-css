# div自适应
一个页面上两个div左右铺满整个浏览器，要保证左边的div一直为100px，右边的div跟随浏览器大小变化（比如浏览器为500，右边div为400，浏览器为900，右边div为800），请写出大概的css代码。

1.横向自适应（弹性布局）


	<style type="text/css" media="screen">
	    * {
	    	margin: 0;
	    	padding: 0;
	    }
		.main {
			width: 100%;
			height: 100px;
			display: flex;
			flex-direction: row;
			align-items: center;
		}
		.fir {
			height: 100%;
			-webkit-flex-basis: 100px;
			flex-basis: 100px;
			background-color: red;
		}
		.sec {
			height: 100%;
			flex-grow: 1;
			background-color: blue;
		}
	</style>

<div class="main">
	<div class="fir"></div>
	<div class="sec"></div>
</div>

2.横向自适应（浮动布局）


	<style type="text/css" media="screen">
	    * {
	    	margin: 0;
	    	padding: 0;
	    }
		.fir {
			height: 100px;
			float: left;
			width: 100px;
			background-color: red;
		}
		.sec {
			height: 100px;
			margin-left: 100px;
			background-color: blue;
		}
	</style>

	<div class="fir"></div>
	<div class="sec"></div>

3.竖向自适应(固定高度div为绝对定位)


	<style type="text/css" media="screen">
	    * {
	    	margin: 0;
	    	padding: 0;
	    }
	    body {
	    	position: absolute;
	    	top: 0;
	    	bottom: 0;
	    	width: 100%;
	    }
	    .container {
	    	height: 100%;
	    }
	    .main {
	    	width: 100%;
	    	height: 100%;
	    	box-sizing: border-box;
	    	padding-top: 100px;
	    	position: relative;
	    }
		.fir {
			position: absolute;
			top: 0;
			left: 0;
			height: 100px;
			width: 100%;
			background-color: red;
		}
		.sec {
			width: 100%;
			height: 100%;
			background-color: blue;
		}
	</style>
<body>
    <div class="container">
	    <div class="main">
		    <div class="fir"></div>
		    <div class="sec"></div>
	    </div>
    </div>   
</body>
4.竖向自适应（为固定div设置margin）

	<style type="text/css" media="screen">
	    * {
	    	margin: 0;
	    	padding: 0;
	    }
	    body {
	    	position: absolute;
	    	top: 0;
	    	bottom: 0;
	    	width: 100%;
	    }
	    .container {
	    	height: 100%;
	    }
	    .main {
	    	width: 100%;
	    	height: 100%;
	    	box-sizing: border-box;
	    	padding-top: 100px;
	    	position: relative;
	    }
		.fir {
			margin-top: -100px;
			height: 100px;
			width: 100%;
			background-color: red;
		}
		.sec {
			width: 100%;
			height: 100%;
			background-color: blue;
		}
	</style>
<body>
    <div class="container">
	    <div class="main">
		    <div class="fir"></div>
		    <div class="sec"></div>
	    </div>
    </div>   
</body>
