中文 | [English](README_EN.md)

###weixinAudio.js
#####一个简单的微信样式播放器
* * *

播放器DOM及CSS是微信里内置的音频播放器的样式，重新创建了控制层js，方便在在公众号，APP等场景使用。

###例子

Take a look at this simple

###如何使用

You may use Vidage on one of the following ways:

###HTML模板

```html
<p class="weixinAudio">
	<audio src="../sound/sound.mp3" id="media" width="1" height="1" preload></audio>
	<span id="audio_area" class="db audio_area">
		<span class="audio_wrp db">
			<span class="audio_play_area">
				<i class="icon_audio_default"></i>
				<i class="icon_audio_playing"></i>
            </span>
			<span id="audio_length" class="audio_length tips_global">3:07</span>
			<span class="db audio_info_area">
                <strong class="db audio_title">标题</strong> 
                <span class="audio_source tips_global">来源</span>
			</span>
			<span id="audio_progress" class="progress_bar" style="width: 0%;"></span>
	 	</span>
	</span>
</p>
```

###Js调用

```html
//你需要先引入一个jQuery
<script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>
<script src="js/weixinAudip.js"></script>
<script>
   $('.jaudio').jAudio(options);
</script>
```

###options/初始化参数

Option | Type | Default | Description
:-- | :--: | :--: | --:
autoplay | Boolean  | true | 播放器是否在初始化时自动播放
src|String|null|如果audeio标签上没设定src属性，可在初始化时设置

###API/执行方法

Method | Parameters | Description
:-- | :--: | --:
play() | ——  | Plays the audio
pause()|——|Pauses the audio
changeSrc(...)|src,callback|src:播放的地址</br>callback:回掉函数

<table width="100%">
<thead>
  <tr>
    <th width="20%">Method</th>
    <th width="15%">Parameters</th>
    <th width="65%">Description</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td><code>play()</code></td>
    <td>&mdash;</td>
    <td>Plays the media</td>
  </tr>
  <tr>
    <td><code>pause()</code></td>
    <td>&mdash;</td>
    <td>Pauses the media</td>
  </tr>
    <tr>
    <td><code>restart()</code></td>
    <td>&mdash;</td>
    <td>Restarts playback</td>
  </tr>
  <tr>
    <td><code>rewind(...)</code></td>
    <td>Number</td>
    <td>Rewinds by the provided parameter, in seconds. If no parameter is provided, the default seekInterval is used (10 seconds).</td>
  </tr>
  <tr>
    <td><code>forward(...)</code></td>
    <td>Number</td>
    <td>Fast forwards by the provided parameter, in seconds. If no parameter is provided, the default seekInterval is used (10 seconds).</td>
  </tr>
  <tr>
    <td><code>seek(...)</code></td>
    <td>Number</td>
    <td>Seeks the media to the provided parameter, time in seconds.</td>
  </tr>
  <tr>
    <td><code>setVolume(...)</code></td>
    <td>Number</td>
    <td>Sets the player volume to the provided parameter. The value should be between 0 (muted) and 10 (loudest). If no parameter is provided, the default volume is used (5). Values over 10 are ignored.</td>
  </tr>
  <tr>
    <td><code>togglePlay()</code></td>
    <td>Boolean</td>
    <td>Toggles playback for the player based on either the boolean argument or it's current state.</td>
  </tr>
  <tr>
    <td><code>toggleMute()</code></td>
    <td>&mdash;</td>
    <td>Toggles mute for the player.</td>
  </tr>
  <tr>
    <td><code>toggleCaptions()</code></td>
    <td>&mdash;</td>
    <td>Toggles whether captions are enabled.</td>
  </tr>
  <tr>
    <td><code>toggleFullscreen()</code></td>
    <td>Event</td>
    <td>Toggles fullscreen. This can only be initiated by a user gesture due to browser security, i.e. a user event such as click.</td>
  </tr>
  <tr>
    <td><code>isFullscreen()</code></td>
    <td>&mdash;</td>
    <td>Boolean returned if the player is in fullscreen.</td>
  </tr>
  <tr>
    <td><code>support(...)</code></td>
    <td>String</td>
    <td>Determine if a player supports a certain MIME type. This is not supported for embedded content (YouTube).</td>
  </tr>
  <tr>
    <td><code>source(...)</code></td>
    <td>Object or undefined</td>
    <td>
      Get/Set the media source.
      <br><br>
      <strong>Object</strong><br>
      See <a href="#source-method">below</a>
      <br><br>
      <strong>YouTube</strong><br>
      Currently this API method only accepts a YouTube ID when used with a YouTube player. I will add URL support soon, along with being able to swap between types (e.g. YouTube to Audio or Video and vice versa.)
      <br><br>
      <strong>undefined</strong><br>
      Returns the current media source url. Works for both native videos and embeds.
    </td>
  </tr>
  <tr>
    <td><code>poster(...)</code></td>
    <td>String</td>
    <td>Set the poster url. This is supported for the <code>video</code> element only.</td>
  </tr>
  <tr>
    <td><code>destroy()</code></td>
    <td>&mdash;</td>
    <td>Destroys the plyr UI and any media event listeners, effectively restoring to the previous state before <code>setup()</code> was called.</td>
  </tr>
  <tr>
    <td><code>restore()</code></td>
    <td>&mdash;</td>
    <td>Reverses the effects of the <code>destroy()</code> method, restoring the UI and listeners.</td>
  </tr>
 </tbody>
</table>