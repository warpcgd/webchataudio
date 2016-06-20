English | [中文](README.md)

###weixinAudio.js
#####一个简单的微信样式播放器/a simple webchat AudioPlayer(from weixin of china)
* * *
播放器DOM及CSS是微信里内置的音频播放器的样式，重新创建了控制层js，方便在在公众号，APP等场景使用。
###例子/Demo
Take a look at this simple
###如何使用/How to use it
You may use Vidage on one of the following ways:
###HTML模板/Add boilerplate/template in your HTML
```html
<p class="jaudio">
	<audio src="../sound/sound.mp3" id="media" width="1" height="1" preload></audio>
	<span id="audio_area" class="db audio_area">
		<span class="audio_wrp db">
			<span class="audio_play_area">
				<i class="icon_audio_default"></i>
				<i class="icon_audio_playing"></i>
            </span>
			<span id="audio_length" class="audio_length tips_global">3:07</span>
			<span class="db audio_info_area">
                <strong class="db audio_title">Title/标题</strong> 
                <span class="audio_source tips_global">From/来源</span>
			</span>
			<span id="audio_progress" class="progress_bar" style="width: 0%;"></span>
	 	</span>
	</span>
</p>
```
###Js调用/Regular way(run js)
```html
//你需要先引入一个jQuery(weixinAudip.js need jQuery)
<script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>
<script src="js/weixinAudip.js"></script>
<script>
   $('.jaudio').jAudio();
</script>
```
###API
