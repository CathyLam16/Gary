var audio = document.getElementById('audios');
function audioAutoPlay(audio){
	play = function(){
		audio.play();
		document.removeEventListener("touchstart",play, false);
	};

	audio.play();
	document.addEventListener("WeixinJSBridgeReady", function () {
		play();
	}, false);

	document.addEventListener('YixinJSBridgeReady', function() {
		play();
	}, false);

	document.addEventListener("touchstart",play, false);
}

//每隔2秒检测是否播放音乐,播放则停止定时器
let t = setInterval(() => {
	if(audio.paused === false){
		console.log('停止定时器');
		clearInterval(t);
	}else{
		console.log('执行定时器');
		audioAutoPlay(audio);
	}
},2000);
