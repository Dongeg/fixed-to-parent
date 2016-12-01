# fixed-to-parent
css相对于父元素做fixed定位

美工一句话，我的一小时·······
```html
<!DOCTYPE html>
<html>
<head>
<title>css相对于父元素做fixed定位</title>
<style type="text/css">
body { 
    background: #ccc;
    height: 2000px ; 
    transform:translateZ(0);/*重点样式*/
    -webkit-transform:translateZ(0);
}
.relative{
	height: 600px;
    width: 650px;
    background: green;
    overflow: auto;
    position: relative;
    left:200px;
    top:100px;
}
.fixed{
	background-color: #ddd;
    width: 300px;
    height: 100px;
    position: fixed;
  	top:200px;
    /*不要设置top,left,bottom,right*/
}
.content{ /*为了撑起absolute的高度*/
  float:left;
  height:1800px;
}
</style>
</head>
<body>
  <div class="relative">
     relative content
    <div class="content"></div>
    <div class="fixed">fixed</div>
  </div>
</body>
</html>
```
