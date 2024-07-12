# 微信视频号下载器

> 🔥🔥🔥 支持加密视频的下载，可到 Release 中下载更新。

- 支持实时捕获视频号的视频地址
- 捕获后，可进行预览和下载
- 支持 Win/Mac

> 内部采用代理拦截请求识别，所以本软件需要安装证书及自动开启代理（当然这些都是自动执行的，无需手动操作）。关闭此软件时会自动清除代理信息，不影响使用。

---

### 效果

1. 运行本软件

2. 打开视频号的视频进行播放，如下图视频：

![image](https://user-images.githubusercontent.com/11046969/169697581-6851f4d1-376b-42c5-825b-8e8101261027.png)

3. 本软件会自动捕获到该视频，可以点击 “预览” 按钮来确认是否拦截正确

![image](https://user-images.githubusercontent.com/11046969/169732758-90685ad1-6092-4c27-bfc5-ff13588f4927.png)



4. 点击 “下载” 按钮进行下载

![image](https://user-images.githubusercontent.com/11046969/169732854-371c5962-b9a1-47da-90a4-d50473e08509.png)


![image](https://user-images.githubusercontent.com/11046969/169698058-5d9f213e-91c7-4f77-872e-db3d983d1a97.png)


---
### 使用

1. 首次打开需要进行初始化，此过程会进行证书安装：

![image](https://user-images.githubusercontent.com/11046969/169732890-9d7af116-d9f3-47cc-a2d7-091b78930c94.png)


2. 点击 “是”，安装后，就可以正常使用了：

![image](https://user-images.githubusercontent.com/11046969/169732926-5c8cfce4-4856-48e2-a268-22e1e5278c2d.png)


#### Mac 系统处理

由于新 Mac OS 不支持非交互式执行 sudo 命令，所以本软件初始化时会自动将命令复制到剪切板，你只需要打开 “终端”，粘贴一下就可以了，然后回车执行，效果如下图所示：

![image](https://user-images.githubusercontent.com/11046969/169732943-4815fa79-dda4-4bfd-904c-70d8e625d8f6.png)

---
#### 本地编译

安装 node, yarn
```
brew install node
brew install yarn
```

启动
```
yarn add concurrently --dev
yarn start
```

#### 打包应用
```
npm run pack
```


FAQ:

问：无法抓包？

答：这个问题主要是缓存的问题(会影响 javascript 脚本注入 polyfills.publishxxx.js)：
windows下清除 C:\Users\<user>\AppData\Roaming\Tencent\WeChat\radium\web\profiles\*
macOS 下清除 ~/Library/Containers/com.tencent.xinWeChat/Data/.wxapplet/web/profiles/multitab*
```
rm -rf Library/Containers/com.tencent.xinWeChat/Data/.wxapplet/web/profiles/multitab*
```
