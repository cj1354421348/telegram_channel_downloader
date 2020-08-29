# telegram_channel_downloader
Telegram 频道/群组 文件下载脚本
脚本需要python3环境，具体安装教程自行搜索。
测试环境  Ubuntu 18.04.5 LTS & Python 3.6.9
**1. 安装**
 
 - 安装redis
 
 安装教程参考 [Redis 安装 | 菜鸟教程](https://www.runoob.com/redis/redis-install.html)
 
 - 安装依赖 
 ```
 pip3 install -U telethon --user
 
 pip3 install cryptg

 pip3 install tqdm
 
 pip3 install redis
 
 pip3 install pillow
 
 pip3 install aiohttp
 
 pip3 install hachoir
 
 ```
 - 从 https://my.telegram.org/apps 获取自己的Telegram API密钥。

 - 下载脚本
 ```
 git clone https://github.com/snow922841/telegram_channel_downloader.git
 ```
**2. 使用**

 - 进入脚本目录

 - 修改telegram_channel_downloader.py文件内的 api_id 和 api_hash 为你自己的

 - 修改脚本内的频道名称、保存路径
 
 - 鉴于网友需要上传GD，特添加了使用gclone自动上传到团队盘的功能，需要在配置区域设置。具体查看脚本内注释
   
 - 运行  
 ```
 python3 tg_channel_downloader.py
 ```
 - 按照提示输入telegram绑定的手机号获取验证码并输入 

<details>
  <summary>点击查看更新日志</summary>
  
  2020-08-19更新
     
   - 添加自动上传到Googledrive的功能
     
   - 使用redis缓存已经遍历的消息ID
 
  2020-08-29更新
  
  - 更换telegram的第三方库
  
  - 默认上传到GD，目前未配置不上传，所以需要安装gclone
  
  - 默认过滤贴纸、动态贴纸、gif格式文件
  
  - 优化了下载和上传进度条的显示
  
  - 上传失败后会把消息ID保存在脚本所在的文件夹，方便以后可以手动下载
  
</details>
