现在版本：Build 2012072141 Pre Alpha V0.11

Now version：Build 2012072141 Pre Alpha V0.11
=======================================================================
简介：
  Oplay,是一款由HTML5+JS编写的音乐播放器，目前支持：
		OGG音乐  （Chrome 还有MP3）
		频谱分析
		歌词同步
		Win8 Metro风格界面
		分辨率响应式（还有BUG）
		节奏分析
		多彩换肤
		全屏支持
	当然，目前播放器还在Pre Alpha，因此还有很多改进空间哦~~~
	另外，由于是初学者，这个播放器90%核心由我自己编写，
	因此代码比较混乱，请多多指教。
=======================================================================
=======================================================================
description：
	Oplay,is a HTML5+JS music player，featured with：
		OGG support  （Chrome with MP3 and ogg）
		audio visiualizer
		Synchronized lyrics
		Win8 Metro UI
		Responsive UI（Still Buging）
		beat detektor
		colorful skin
		full screen support
	Ofcourse，the player is on its Pre Alpha now，
	So,its not done yet~~~
	otherwise，cause i'm a newbie and a student，About 90 percent 
	of the code is done by myself，
	So,the code is a mess，Please exhibitions。
=======================================================================
**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay
=======================================================================
开源信息：

主源码站：https://github.com/scientihark/oplay （GIT）
Google Code镜像：https://code.google.com/p/oplay-scientihark/ （SVN）
=======================================================================
=======================================================================
Opensource Information：

main source：https://github.com/scientihark/oplay （GIT）
Google Code mirror：https://code.google.com/p/oplay-scientihark/ （SVN）
=======================================================================
**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay
========================================================================
授权信息:

*  请注意 Oplay 根据GNU GPL V3 协议开源。
*  你应该在License目录找到 GNU General Public License
*  如果没有请到 <http://www.gnu.org/licenses/> 获取协议.
*
*  如果需要其他授权，请联系 mgbbs.mobile@gmail.com。

*另外，由于使用了一些开源库，因此，保留以下授权信息：
* MIT License [http://www.opensource.org/licenses/mit-license.php]
========================================================================
========================================================================
Licensing Information：

*  Please note that Oplay are licensed under the terms of GPL version 3.
*  You should have received a copy of the GNU General Public License
*  along with this program.  If not, see <http://www.gnu.org/licenses/>.
*
*  Please contact mgbbs.mobile@gmail.com if you seek alternate
*  licensing terms for your project.

* Also，I used some opensource libs，so License below are required：
* MIT License [http://www.opensource.org/licenses/mit-license.php]
========================================================================
**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay**Oplay
========================================================================
版本信息：

Build 2012071402 Pre Alpha V0.1

	现在pre alpha暂不开源哦.alpha出后一定开源github

Build 2012071504 Pre Alpha V0.1a

	--修正了歌词算法，目前歌词基本同步了。
	--添加播放列表分页支持
	--播放列表伪3D特效

Build 2012071812 Pre Alpha V0.1b

	--播放列表伪3D特效加强
	--添加歌词秀背景
	--添加多分辨率响应式支持（歌词字体响应式bug中）
	--添加响应式自动分页
	--添加全屏功能

Build 2012071821 Pre Alpha V0.1c

	--添加chrome的波谱分析（still buging 见下）

Build 2012071910 Pre Alpha V0.1d

	--添加history push 现在每一首歌都有播放历史了，而且可以通过点击(http:xxxxxx/index.html?4234|:|ggggg)的方式直接播放指定音乐。

Build 2012072141 Pre Alpha V0.11

	--添加ID3信息获取，现在可以从音乐中直接获取歌手、album、album pic等信息了（部分音乐的ID3 TAG编码问题导致中文乱码，目前暂无法解决）

						by scientihark
========================================================================
========================================================================
Change Log:

Build 2012071402 Pre Alpha V0.1

	Now oplay is on its pre alpha.when alpha is out ,the source will be available on github.

Build 2012071504 Pre Alpha V0.1a

	--Fixed Lyrics algorithm，Currently,Lyrics synchronous。
	--Add playlist paging support
	--Playlists 3D effects

Build 2012071812 Pre Alpha V0.1b

	--Strengthen the 3D effects of the playlist
	--Add the lyrics show background
	--add Responsive support for multi-resolution（Lyrics fonts size still buging）
	--Add Responsive automatic paging for playlist
	--Add full-screen support

Build 2012071821 Pre Alpha V0.1c

	--Add audio visiualizer for chrome (still buging read more blow)

Build 2012071910 Pre Alpha V0.1d

	--add history push ,now each song has a player history，And by clicking(http:xxxxxx/index.html?4234|:|ggggg)you can play the choosed sond directly。

Build 2012072141 Pre Alpha V0.11

	--add ID3 tag information，You can now get singer album album pic and other information from the music (some of the song with special encoding can cause Chinese garbled）

						by scientihark
============================================================================
============================================================================
目前已知：

由于W3c Audio标准制定中（这类API将十分底层）
firefox 13+最完整特性：

	Audio --播放  （OGG）
	transction --2D动画特效（基本界面、歌词秀动画、歌词秀背景）
	transfrom --伪3D动画特效（专辑动画，播放列表动画）
	XHR--歌词秀
	Audio API --播放控制，歌词同步
	Audio Data API (MOZ版)--码率、声道、波谱分析、节奏分析（未来均衡器、合成、环境等等）
	CSS3 media screen --多分辨率响应式（自动化响应由js辅助）

Chrome目前
	
	还不支持Audio Data API(MOZ版)，而是用webkitcontext+buffer,小试了下，太复杂。不好整合。因此，chrome 木有码率、声道，其他不错（OGG音质弱于MOZ）
	经过技术研究，Audio API问题基本解决了（使用了createMediaSourceElement 将MOZ的audio DATA API 和 webkit的web audio api融合解决了数据流问题。），但是目前chrome存在bug,createMediaSourceElement绑定Audio对象后如果修改SRC就会出现 crash(18)|| 声音诡异变速（数据流BUG，JS无法解决）（19~22【22.0.1210.0 (147194)】），
	因此chrome播放第一首歌完美（波形的平滑度远高于moz,但ogg音质较差)，大家可以自己决定是否预览（要预览的，开始播放前 在console 敲入$webkitloaded=1;）;


Opera目前
	不支持Audio Data API(MOZ版) 木有码率、声道、波谱分析
	不支持transction 2D动画特效

IE目前
	额~~
	IE8好像木有支持的
	加了HTML5支持库的IE9木有测试
	IE10木有测试，应该可用

safari 我的safari挂了，木有测.不过webkit应该和chrome差不多

目前有纯js的mp3,flac,alac,aac,wav解码器，但是太复杂，暂时木有用。
===========================================================================
============================================================================
Currently known：

With the W3c Audio standard still setting（those api may be really low-layer）

firefox 13+ has the full feature：

	Audio --play  （OGG）
	transction --2D Animation（basic UI、LRC UI、LRC BG）
	transfrom --3D Animation（Album pic animation，playlist animation）
	XHR--LRC
	Audio API --player control，Synchronized lyrics
	Audio Data API (MOZ)--Bit rate channel audio visiualizer beatdetektor（will add Equalizer、Synthesizer、Environment and so on）
	CSS3 media screen --Responsive UI（I write some javascript that help）

Chrome :
	
	not support Audio Data API(MOZ)，but using webkitcontext+buffer,I tried，but it's too difficult。so，chrome don't have audio visiualizer and beatdetektor

	After technical studies，I basically solved the problem（use createMediaSourceElement to mearge MOZ's audio DATA API with  webkit's web audio api），But chrome is still buging,after createMediaSourceElement connetced to Audio element,if you change the src : 	
	chome will crash(chrome 18)
	the sound sounds strange（chrome's BUG，can not solve with JS）（19~22【22.0.1210.0 (147194)】）
	To preview this change，run $webkitloaded=1; in console before you start playing;

Opera:
	not support Audio Data API(MOZ)
	not support transction

IE目前
	e~~
	IE8 and below seemed not working at all
	IE9 can play music
	I haven't test IE9 with htm5.js
	I haven't test IE10.

safari:
	my safari crashed，so I haven't test yet.but I think it may be same as chrome

Now there are mp3,flac,alac,aac,wav decoder in pure javascript ，but it's a little difficult。
===========================================================================
