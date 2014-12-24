AndroidMultiChannelBuildTool
============================

安卓多渠道打包工具。   
实现思路讲解： [Android批量打包提速 - GavinCT](http://www.cnblogs.com/ct2011/p/4152323.html)  

使用本工具，Android程序员仅需将ChannelUtil.java放入到工程里使用，以后打包的事情就不用自己动手了。  
安装个Python环境，双击一下MultiChannelBuildTool.py，谁都可以打包了！
# 目录介绍及使用注意
## PythonTool
Python2 与 Python3 都能正常使用 

- info目录下的channel用来存放渠道，多个渠道之间用换行隔开。  
  注意：  
  fork后通过Github clone，这个channel文件在Windows端是正常的，以换行隔开。  
  直接点击右侧的download下载zip，可能你在windows端看到的就不是以换行隔开的。  
  这是Github造成的。
- MultiChannelBuildTool.py是多渠道打包的脚本。

## JavaUtil
ChannelUtil.java 用来解析渠道，直接拷贝到Android工程中使用即可。  
ChannelUtil中的getChannel方法可以方便的获取渠道。 

# 常见问题答疑 

这部分问题是由美团大神<a href="http://weibo.com/coderdd" target="_blank" >丁志虎</a>在微博上答复的，摘录如下：

- 这个方案没法解决不同渠道使用渠道自己SDK的问题，友盟的SDK提供了在代码中设置渠道的方式，所以再获取到渠道号后再调用SDK相关设置渠道的方法就可以了
- apk用的是java那一套签名，放在META-INF文件夹里的文件原则上是不参与签名的。如果Google修改了apk的签名规则，这一套可能就不适用了。

# License

    Copyright 2014 GavinCT

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


