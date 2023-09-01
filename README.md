# Tesla-Cam-Timer
### 轻量级的为特斯拉行车记录仪加时间水印的工具  
杭州交通违法举报要求上传违法过程的视频作为证据，但要求视频中有时间码水印，特斯拉的记录仪不带这玩意，因此被拒绝采纳作为证据，手机拍屏幕带上时间信息也不行，所以做了这个工具（~~但做好了目前还没遇到违法行为，无法测试效果。。~~）  
已通过本工具成功举报了两次实线变道，收到奖励10元🫡

<p align="left">
<img width="300" alt="Screen Shot" src='https://raw.githubusercontent.com/bigxixi/bigxixi.github.io/master/teslaCamTimer/0.jpg' />
</p>

[👉🏻体验地址](https://bigxixi.com/teslaCamTimer/) 

### 使用步骤：

可以在电脑也可以在手机使用本工具。[▶️视频操作演示](https://www.bilibili.com/video/BV1Pu4y1D7ND/)   
如果是电脑，直接将U盘插入电脑，然后从步骤4开始看；  
如果是手机，请使用手机浏览器（Safari/Chrome），微信等APP直接打开链接有可能无法使用：  
1.根据手机类型（安卓、苹果）准备好OTG转接头。 

<p align="left">
<img width="300" alt="Screen Shot" src='https://raw.githubusercontent.com/bigxixi/bigxixi.github.io/master/teslaCamTimer/2.jpg' />
</p>

2.取下行车记录仪U盘，插入转接头连上手机。  
3.打开文件管理器确认U盘是否链接成功。  

 `注意:视频文件名不要改!`
 
<p align="left">
<img width="300" alt="Screen Shot" src='https://raw.githubusercontent.com/bigxixi/bigxixi.github.io/master/teslaCamTimer/1.jpg' />
</p>  

4.点击「选择文件」，进入特斯拉U盘选取视频片段。特斯拉记录的视频是每个片段1分钟。  
5.点击「开始录制」，等待录制（可以滑动进度条到对应时间点再开始）。  
6.点击「结束录制并下载视频」完成录制。  
7.点击浏览器的下载列表，可以看到刚才录制的视频。  

`iPhone（Safari）生成的是mp4格式，安卓（Chrome，edge）生成的是webm，如需转换为mp4，可以搜索一些在线工具或者app，例如` 
https://converter.app/webm-to-mp4/

### 源码
源码全都在`index.html`一个文件里，没有服务端设置，下载到本地双击打开就可以使用，主要利用了canvas.captureStream()和mediaRecorder调用浏览器原生的能力来生成视频，因此不同浏览器生成的视频格式不一样，iPhone（Safari）生成的是mp4格式，安卓（Chrome，edge）生成的是webm，另外手机性能会影响生成视频的流畅程度（主流手机应该没啥问题，老旧低端机会卡顿）
