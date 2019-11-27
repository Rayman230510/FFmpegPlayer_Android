#这是基于Android，集成FFmpeg动态库，制作的简单播放器

1. 涉及到的技术点
   +Android jni
   +FFmpeg动态库编译以及FFmpeg相关编解码以及播放接口
   +OpenSLES音频库相关接口调用
   +ANativeWindow的绘制

2. 优势
   +相比Android原生播放器播放速度更快，原因如下：
      +Android原生的播放器在播放数据时候，AudioTrack在播放pcm时候会将数据从java层拷贝到jni层
	  +使用OpenSLES库，减少了在java层和jni之间拷贝数据的动作
	  +FFmpeg支持的完整的音视频数据格式转换

3. 目的
   +学习相关库的使用
   +自我提升