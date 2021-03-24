
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Happy Birthday To U</title>

<style type="text/css">
@font-face {
	font-family: digit;
	src: url('digital-7_mono.ttf') format("truetype");
}
</style>

<style>
    body{margin:0;padding:0;background:#ffe;font-size:12px;overflow:auto}
    #mainDiv{width:100%;height:100%}
    #loveHeart{float:left;width:670px;height:625px}
    #garden{width:100%;height:100%}
    #elapseClock{text-align:right;font-size:18px;margin-top:10px;margin-bottom:10px}
    #words{font-family:"sans-serif";width:500px;font-size:24px;color:#666}
    #messages{display:none}
    #elapseClock .digit{font-family:"digit";font-size:36px}
    #loveu{padding:5px;font-size:22px;margin-top:80px;margin-right:120px;text-align:right;display:none}
    #loveu .signature{margin-top:10px;font-size:20px;font-style:italic}
    #clickSound{display:none}
    #code{float:left;width:440px;height:400px;color:#333;font-family:"Consolas","Monaco","Bitstream Vera Sans Mono","Courier New","sans-serif";font-size:12px}
    #code .string{color:#2a36ff}
    #code .keyword{color:#7f0055;font-weight:bold}
    #code .placeholder{margin-left:15px}#code .space{margin-left:7px}
    #code .comments{color:#3f7f5f}
    #copyright{margin-top:10px;text-align:center;width:100%;color:#666}
    #errorMsg{width:100%;text-align:center;font-size:24px;position:absolute;top:100px;left:0}
    #copyright a{color:#666}
</style>

<script type="text/javascript" src="js/jquery.js"></script>
<script type="text/javascript" src="js/garden.js"></script>
<script type="text/javascript" src="js/functions.js"></script>

</head>

<body>
<div style="text-align:center;clear:both;">
<script src="/gg_bd_ad_720x90.js" type="text/javascript"></script>
<script src="/follow.js" type="text/javascript"></script>
</div>
<div id="mainDiv">
	<div id="content">
		<div id="code">
			<span class="comments">/*</span><br />
			<span class="space"/><span class="comments">*2020—02-01,</span><br />
			<span class="space"/><span class="comments">*2021-03-25.</span><br />
			<span class="space"/><span class="comments">*/</span><br />
			<span class="keyword">String</span> 🐷 = <span class="comments">"Mark béo"</span>;<br />
			<span class="keyword">String</span> ❤ = <span class="comments">"Love"</span>;<br />
			<span class="keyword">String</span> 🐯 = <span class="comments">"Jane thối"</span>;<br />

			for (<span class="keyword">int</span> <span class="string">i</span>=0; 
			<span class="string">i</span><=<span class="string">Date</span>() ; 
			<span class="string">i</span>++)<br>
			{<br>
				<span class="placeholder"/><span class="string">print</span>(🐷,❤,🐯)<br>
			}<br>
			
			<br>
		</div>
		<div id="loveHeart">
			<canvas id="garden"></canvas>
			<div id="words">
				<div id="messages">
					親愛的，生日快樂!
					<div id="elapseClock"></div>
				</div>
				<div id="loveu">
					爱你直到永永遠遠。<br/>
					<div class="signature">- 明洲</div>
				</div>
			</div>
		</div>
	</div>
</div>

<script type="text/javascript">
var offsetX = $("#loveHeart").width() / 2;
var offsetY = $("#loveHeart").height() / 2 - 55;
var together = new Date();
together.setFullYear(2020, 2, 01);
together.setHours(20);
together.setMinutes(0);
together.setSeconds(0);
together.setMilliseconds(0);

if (!document.createElement('canvas').getContext) {
	var msg = document.createElement("div");
	msg.id = "errorMsg";
	msg.innerHTML = "Your browser doesn't support HTML5!<br/>Recommend use Chrome 14+/IE 9+/Firefox 7+/Safari 4+"; 
	document.body.appendChild(msg);
	$("#code").css("display", "none")
	$("#copyright").css("position", "absolute");
	$("#copyright").css("bottom", "10px");
	document.execCommand("stop");
} else {
	setTimeout(function () {
		startHeartAnimation();
	}, 5000);

	timeElapse(together);
	setInterval(function () {
		timeElapse(together);
	}, 500);

	adjustCodePosition();
	$("#code").typewriter();
}
</script>

</body>
</html>
