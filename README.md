<img width="768" src="https://github.com/openwrt/openwrt/blob/main/include/logo.png"/>

## 特别提示 [![](https://img.shields.io/badge/-个人免责声明-FFFFFF.svg)](#特别提示-)

- **本人不对任何人因使用本固件所遭受的任何理论或实际的损失承担责任！**

- **本固件禁止用于任何商业用途，请务必严格遵守国家互联网使用相关法律规定！**

## 本仓库的结构
```
通用云编译模板
你的 GitHub 仓库结构：
├── .github/
│   └── workflows/
│       └── build.yml          <- 上面这个 workflow 文件 
├── configs/
│   └── recs07.config          <- 编译配置文件           
├── diy-script.sh              <- 自定义补丁/设置脚本    
└── README.md
使用教程也非常简单
只需要改这几项变量即可：
env:
  REPO_URL: https://github.com/immortalwrt/immortalwrt.git     # 改源码
  REPO_BRANCH: openwrt-21.02                                   # 改分支
  CONFIG_FILE: configs/x86_64.config                           # 改 config

```                                           

## 项目说明 [![](https://img.shields.io/badge/-项目基本介绍-FFFFFF.svg)](#项目说明-)
- 固件默认管理地址：`192.168.1.1` 默认用户：`root` 默认密码：`password`
- 源码：[LiBwrt](https://github.com/LiBwrt-op/openwrt-6.x)
- 源码：[immortalwrt](https://github.com/immortalwrt/immortalwrt)
- 源码：[LEDE](https://github.com/coolsnowwolf/lede)
- 源码：[VIKINGYFY](https://github.com/VIKINGYFY/immortalwrt)
- 云编译来源：https://github.com/haiibo/OpenWrt


## 定制固件 [![](https://img.shields.io/badge/-项目基本编译教程-FFFFFF.svg)](#定制固件-)
1. 首先要登录 Gihub 账号，然后 Fork 此项目到你自己的 Github 仓库
2. 修改 `configs` 目录对应文件添加或删除插件，或者上传自己的 `xx.config` 配置文件
3. 插件对应名称及功能请参考恩山网友帖子：[Applications 添加插件应用说明](https://www.right.com.cn/forum/thread-3682029-1-1.html)
4. 如需修改默认 IP、添加或删除插件包以及一些其他设置请在 `diy-script.sh` 文件内修改
5. 添加或修改 `xx.yml` 文件，最后点击 `Actions` 运行要编译的 `workflow` 即可开始编译
6. 编译大概需要3-5小时，编译完成后在仓库主页 [Releases] 对应 Tag 标签内下载固件

如果你觉得修改 config 文件麻烦，那么你可以点击此处尝试本地提取 https://github.com/LiBwrt/openwrt-6.x

**如果看不懂编译界面可以参考 YouTube 视频：[软路由固件 OpenWrt 编译界面设置](https://www.youtube.com/watch?v=jEE_J6-4E3Y&list=WL&index=7)**

## 小白使用云编译教程
1. 只需要修改workflows里面的yml文件中的REPO_URL变量后面的值，改为你需要编译的openwrt源代码地址就行，然后再更改REPO_BRANCH的分支就行。
2. 如何查看REPO_BRANCH的分支能，找到源代码地址，然后点击branch就能查看了
3. diy_script.sh可以修改路由器固件的ip地址，以及主机名，自己看注释合理修改即可
4. 以上环节弄好之后就可以点击action，找到你需要启动编译的yml就行，开始编译

enjoy~


<a href="#readme">
<img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" title="返回顶部" align="right"/>
</a>
