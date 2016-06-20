###weixinAudio.js
#####a simple webchat AudioPlayer(from weixin of china)
* * *
微信推文里内置的音频播放器样式，我将其改写为HTML5 Video，使其能在公众号中使用。
###Demo
Take a look at this simple
###How to use it
You may use Vidage on one of the following ways:
###Add boilerplate/template in your HTML
```html
<p class="jaudio">
			<audio src="../sound/sound.mp3" id="media" width="1" height="1" preload></audio>
			<span id="audio_area" class="db audio_area">
				<span class="audio_wrp db">
					<span id="voice_play_MzA4NzEzMjYxN181MDIxMjY2NzQ=_0" class="audio_play_area">
					<i class="icon_audio_default"></i>
					<i class="icon_audio_playing"></i>
					<img src="http://res.wx.qq.com/mmbizwap/zh_CN/htmledition/images/icon/appmsg/audio/icon_audio_unread26f1f1.png" alt="" class="pic_audio_default">
                </span>
				<span id="audio_length" class="audio_length tips_global">3:07</span>
				<span class="db audio_info_area">
                	<strong class="db audio_title">Title/标题</strong> 
                	<span class="audio_source tips_global">From/来源</span>
				</span>
				<span id="audio_progress" class="progress_bar" style="width: 0%;"></span>
				</span>
		</p>
```
###Regular way/js init
```html
//你需要先引入一个jQuery(weixinAudip.js need jQuery)
<script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>
<script src="js/weixinAudip.js"></script>
<script>
   $('.jaudio').jAudio();
</script>
```