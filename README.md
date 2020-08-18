## 基于hexo的个人博客
> 在线预览：https://whalezhang.github.io  


### 说明
> 目前仅对博客中的部分配置内容进行了修改，不多赘述，更多博客模板配置详情请看大佬的博客内容


1. 感谢**Sitoi**大佬，使用了其提供的博客模板：https://github.com/Sitoi/Sitoi-blog.git

2. 设置滚动时顶部导航栏的背景色：http://color.oulu.me/


css修改地址： `themes\matery\source\css\matery.css`
```
.bg-color {
    /* 替换此样式进行修改 */
    /* background-image: linear-gradient(to right, #1f4d71 0%, #71bbb6 100%); */
    background-image: linear-gradient(-225deg, #2CD8D5 0%, #6B8DD6 48%, #8E37D7 100%);
    opacity: 0.9;
}
```
3. 看板娘设置
- 使用 npm 在 hexo 下安装 hexo-helper-live2d，它将 live2d-widget.js 与 hexo 进行了整合
```
# live2d 插件
npm install --save hexo-helper-live2d

# live2d某模型看板娘，可根据喜好更换
npm install live2d-widget-model-shizuku
```
- 安装成功就可以在 node_modules 目录中找到 live2d-widget 和 live2d-widget-model-shizuku 两个目录
- 修改`_config.yml`，添加如下配置
```
live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  log: false
  model:
    # 此处是配置根据下载的看板娘模型可以选择你喜欢的看板娘
    use: live2d-widget-model-koharu
  display:
    position: right
    width: 150
    height: 200
  mobile:
    show: true
  react:
    opacity: 0.9
```
