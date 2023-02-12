# NodeMediaClient-Android
[![](https://jitpack.io/v/NodeMedia/NodeMediaClient-Android.svg)](https://jitpack.io/#NodeMedia/NodeMediaClient-Android)   
一个简单，快速，免费的直播SDK.  

# 用Gradle导入
```
allprojects {
    repositories {
        google()
        jcenter()
        maven { url 'https://jitpack.io' }
    }
}
```

## 新版 gradle 7.2以上 ，settings.gradle
```
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
        maven { url 'https://jitpack.io' }
    }
}
```

```
dependencies {
    implementation 'com.github.NodeMedia:NodeMediaClient-Android:2.9.23'
    
    
}
```
# 简单用法
完整用例：[QLive源码](https://github.com/NodeMedia/QLive-Android)[(API文档)](https://github.com/NodeMedia/NodeMediaClient-Android/tree/2.x/docs)

# 特性
## NodePlayer
* 专为RTMP/RTSP等直播协议优化的码流解析器，极短的分析时间，秒开视频流
* NEON指令集优化的软件解码器，性能好，兼容性强
* 视频编码:H.265/H.264支持硬解码
* 支持的网络协议 RTMP/RTMPT/RTMPE/RTSP/HLS/HTTP(S)-FLV/KMP
* 支持的视频解码器:H.264, H.265
* 支持的音频解码器:AAC, SPEEX, NELLYMOSER, G.711
* OpenGL ES视频渲染
* 全自动网络异常重连
* 支持播放中途来电保持网络流，暂停播放，挂机后继续播放
* 支持设置最大缓冲时长,杜绝延迟累计
* 支持多路直播流同时播放
* RTMP支持设置swfUrl和pageUrl
* RTMP支持设置Connect Arguments (rtmpdump风格)
* RTMP支持Adobe auth模式的鉴权验证 如rtmp://user:pass@server:port/app/name
* RTMP支持发送FCSubscribe命令，兼容国外Akamai, Edgecast , Limelight 等CDN
* RTSP支持的传输协议: TCP/UDP/UDP_MULTICAST/HTTP
* RTSP支持海康Smart265解码播放
* 支持RTMP/HTTP-FLV视频解密播放

## NodePublisher
* H.264/H.265+AAC 组合的RTMP协议音视频流发布
* 全屏视频采集，1080p原画质缩放
* NEON指令集优化H.264软件编码器，性能强劲，兼容性极强
* H.264支持Baseline, Main, High profile
* 支持H.264/H.265 硬编码
* 支持手机旋转,横屏16:9，竖屏9:16分辨率自动输出横竖屏视频流
* 支持4:3分辨率,1:1分辨率输出
* NEON优化AAC软件编码器，极少CPU占用，支持LC和HE profile，音质还原效果好
* 支持SPEEX音频编码
* 支持环境背景噪音抑制
* 支持发布中途切换前后摄像头
* 支持闪光灯开关
* 支持全时自动对焦与手动对焦切换
* 支持单音频流发布
* 支持发布中途来电保持网络流，暂停发布，挂机后继续发布
* 支持预览摄像头后,任意时刻截图
* 内置基于GPU加速的5级磨皮美白滤镜
* 支持动态设置视频码率
* 支持视频码率自适应网络带宽
* 支持GPU算法的镜头缩放,兼容性好
* 支持RTMP视频加密推流

# 支持的流媒体服务端
fms, wowza, evostream, red5, crtmpserver, nginx-rtmp-module, srs, [Node-Media-Server](https://github.com/illuspas/Node-Media-Server) 及其他标准RTMP协议服务端

# 跨平台开源流媒体服务端
[Node-Media-Server](https://github.com/illuspas/Node-Media-Server) 
基于Node.JS开发, 跨平台/高性能, 支持RTMP协议推流,RTMP/HTTP-FLV/WebSocket-FLV播放, 内置推流鉴权/播放防盗链/GOP缓存急速秒开.

# 高级版
- 硬件加速的视频编解码器
- 麦克风降噪
- 平滑肌肤美颜
- RTMP音视频内容加密

请联系商务服务  
邮箱 : service@nodemedia.cn  
QQ : 281269007
