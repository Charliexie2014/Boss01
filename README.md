<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
 
  <title>Document</title>
  <style type="text/css">

  body,ul,li{
  margin:0px;
  padding:0px;
  
  }
  ul,li{list-style:none}
  body {
  background-color:#ccc;
  font-size:14px;
  
  }
  .box{
  width:1000px;
  
  margin:0px auto;
  background-color:white;
  border:1px solid red;
  }
  header{
  height:60px;
  line-height:60px;
  background-color:#990000;
  text-align:center;
  font-family:楷体;
  color:white;
  font-size:30px;
  }
  nav{
  height:40px;
  line-height:40px;
  background-color:#ff99ff;
  }
  nav li{
  float:left;
  border:1px solid red;
  background-color:#cc9966;
  color:white;
  padding:0px 10px;
  font-size:18px;
  font-weight:bold;
  font-family:黑体;

  }
  section{
  width:800px;
  height:500px;
  border:1px solid red;
  
  float:left;
  }
  aside{
  width:190px;
  height:500px;
  background-color:#999966;
   border:1px solid red;
  float:right;
  }
  footer{
  height:40px;
  line-height:40px;
  text-align:center;
  color:white;
  background-color:#cc6699;
  clear:both;
  }

  #dome{
  width:150px;
  height:500px;
  border:1px dashed red;
  margin:0px auto;
  padding:0px 16px;
  color:blue;
  background-color:#cc3399;
  font-weight:bold;
  overflow:hidden;//超出的部分隐藏
  }
  #dome li{
  padding:9px 0px;
  }
  </style>

 </head>
 <body>
 <div class="box">
 <header>HTML5排版练习</header>
 <nav>
 <ul>
 <li>header网页头部</li>
 <li>nav导航栏/菜单栏</li>
 <li>footer页脚信息</li>
 </ul>
</nav>
<section>
<article>
<details><b>识人法则</b></details>
<p>美国惠普公司总裁曾经说过：若是你泛泛去遴选一件商品，遴选一件通俗的物品，你很有可能会让其他人代庖，可是你给太太遴选钻石的时辰，绝对不会请别人代庖，而是本身亲自遴选。</p>
<p>挑钻石要亲自<mark>遴选</mark>，挑通俗的商品要请别人代庖，在惠普公司办理层眼里，他们把优异的员工当成钻石一样，既然是挑钻石，就不成能请其他人代庖，每一个办理者都必需亲自面试。
在中国良多不职业化公司存在如许的现象，良多办理者不注重若何面试员工，也不进修怎么面试员工，他们认为这是人力资本部的工作，这是不职业化的思惟。

</p>
</article>
<progress id="pro" style="width:800px;" max="100" value="0"></progress>
<img width=800px height=350px src="px.jpg" />
<script>
//获取对象
var pro=document.getElementById("pro");
var i=0;
window.setInterval("star2()",100);
function star2(){
pro.value=i;
i++;
if(pro.value==pro.max){
i=0;
}
}

</script>
</section>


<aside>
<div id="dome" >
	<div id="dome1">
		<ul>			
			<li>2017节假日安排</li>
			<li>男婴被弃绿化带</li>
			<li>人民警察法拟大修</li>
			<li>冷空气今袭中东部</li>
			<li>为留员工帮找对象</li>
			<li>关之琳复出</li>
			<li>关晓彤晒照迪士尼</li>
			<li>84岁济公演戏</li>
			<li>主播直播宜家过夜</li>
			<li>香港的哥偷拍哺乳</li>
			<li>生育水平全球最低</li>
			<li>你的名字票房破亿</li>
			<li>女童惨死停车场</li>
			<li>盗后睡15小时</li>
			<li>潜水遭教练袭胸</li>
		</ul>
	</div>
	<div id="dome2"></div>
 </div>
  <script>
  window.onload=function (){
	//获取3个Div的id
  var dome =document.getElementById("dome");
  var dome1 =document.getElementById("dome1");
  var dome2 =document.getElementById("dome2");
	//获取3个DIV的高度
   dome1.style.height=dome.offsetHeight+"px";
   dome2.style.height=dome.offsetHeight+"px";
	//将dome1的内容拷贝到dome2中
   dome2.innerHTML=dome1.innerHTML;
   //dome的scrllTop属性来实现滚动
   window.setInterval("start2(dome)",20);

  }
  function start2(dome){
  if(dome.scrollTop==dome.offsetHeight){
	dome.scrollTop=0;
  }else{
	dome.scrollTop++;//向上滚动的距离
	}
  }
  
  </script>
</aside>
<audio controls="controls" src="美丽的神话.mp3">对不起,不支持</audio>
<!--autoplay="autoplay"自动播放-->

<video controls="controls" poster="px.jpg" src="my girl主题曲.mp4">对不起,不支持</video>
<form name="form1" method="post" action="login.php">
用户名:<input type="text" name="username"/>
密码:<input type="password" name="userpad"/><br>

颜色选择:<input type="color" name="color" ><br>
邮箱:<input type="email" name="email" ><br>
网址:<input type="url" name="url" ><br>
日历:<input type="date" name="date" ><br>
<input type="submit" value="提交表单">
</form>

 <footer>HTML版权所有-Charlie-2014</footer>

 </div>
  
 </body>
</html>

