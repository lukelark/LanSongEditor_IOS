# LanSongEditor_IOS
lansong  video  editor   ios version. crop cut overlay  filter beautiful compress merge and so on...
 蓝松科技的视频编辑SDK IOS版本Demo演示.
 
###注意: 当前版本是1.4.0. 
	MediaEditor和MediaInfo,支持预览功能.
	当前已有的画笔有: 视频画笔, UI画笔,图片画笔, 摄像机画笔.
	


###此SDK采用为收费授权,公司性质的合作,为了您项目更好的进行,欢迎和我们联系.谢谢!

###画板和画笔架构
*   一个工程是由多个线程组成, 又由各种类对象组成. 
*   我们把对视频处理的OpenGL技术处理后封装成 线程，命名为DrawPad(画板)
*   对视频处理用到的各种素材，封装成类，命名为Pen(画笔)
*   这样视频处理的OpenGL线程中增加的各种类对象，就被抽象成 画板和画笔的关系。和日常画画流程一致，方便您的使用。
*   画板：用来处理各种素材的线程，分为 [画板前台线程] 和 [画板后台线程], 您自由选择使用。
*   画笔：编辑会用到的素材。包括：视频，图片，文字，音乐，麦克风，摄像头，裸数据，MV等。这些经过我们的核心技术处理，变成：视频画笔， 		图片画笔，UI画笔，音乐画笔，麦克风画笔，数据画笔，摄像头画笔，MV画笔等。
*   抽象类Pen：继承它的有：视频画笔， 图片画笔，UI画笔，数据画笔，摄像头画笔，MV画笔；均有：平移/缩放/旋转/隐藏/显示/RGBA调节的功能。
		另外他们各自也有独立的方法。
*   滤镜功能：具有滤镜属性的画笔有：视频画笔，图片画笔，摄像头画笔


比如您的操作是：
1.	把给视频增加滤镜： 则你增加视频画笔到画板上， 然后调节VideoPen中的滤镜属性即可。

2.	再比如： 你要在视频中增加文字： 则你增加[视频画笔]+[UI画笔]到画板中，在处理过程中，实时的调节他们即可。

3.	再比如：你要拍照的同时增加滤镜，或增加图片或视频在四周环绕， 则您可以增加[摄像头画笔]+[图片画笔]或[视频画笔]到画板上，图片设置到四周，视频用滤镜处理成中间透明，就实现您要的效果。

4.	再比如：你想生成一段文字或把炫酷的动画转换为视频，则可以直接增加[UI画笔]到画板上。

5.	再比如：你想给视频实时增加说话声，则可以直接增加[Mic画笔]，当然如果仅仅是剪切替换声音，则直接用VideoEditor类中的替换方法就可以。

											


###更仅一步说:
*	1，你用 【视频画笔 VideoPen】在 画板 DrawPad上作画， 就得到 调整后的视频

* 2，你用  【图片画笔 BitmapPen】在画板上作画， 就得到 动态的照片影集。

*	3，你用 【UI画笔  ViewPen】在画板上作画， 就是把精美的UI界面转换为视频， 当然我们的设计，也可以后台处理。

* 4， 你用 【视频画笔】+ 【图片画笔】 在画板上作画， 就得到动态的视频图片效果。

* 5， 你用  【视频画笔】 + 【MV画笔】 在画板上作画， 就是在视频中叠加MV的效果。

* 6， 当然： 画板 可以在前台工作， 也可以在后台处理。



###下载地址: 
*  https://github.com/LanSoSdk/LanSongEditor_IOS

###我们有android版本的SDK，欢迎你的评估使用：
*	android系统SDK--基本版本：https://github.com/LanSoSdk/LanSoEditor_common
*	android系统SDK--高级版本：https://github.com/LanSoSdk/LanSoEditor_advance

###联系方式:
*   QQ 1852600324 
*   Email:support@lansongtech.com
*   网站: www.lansongtech.com