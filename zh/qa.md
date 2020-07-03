# 常见问题

## 插件无法启动

目前已知插件无法在较低版本的 VSCode 上运行，建议升级 VSCode（本人使用的是 1.46.1）。

> 已知原因：
> - 使用了 `vscode.workspace.fs` 对象进行文件读写，该对象在较低版本的 VSCode 上没有提供。

## 如何自定义语音包

请参阅：http://saekiraku.github.io/#/zh/voice-packages.md

## 能否支持更多的语言/编辑器/IDE

单纯的根据语音包的[结构定义](voice-packages.md)扩展关键字很容易，困难的是缺少优质的语音资源和文案。这也是为什么我要在 README 里单独并且着重声明了使用多媒体资源时的权利和义务。其实我根本不在乎项目代码是否遵循了什么协议而被使用，因为这些远不如产品与资源层面的东西重要。

对于编辑器或IDE，由于我平时工作中只使用 VSCode 搭配插件，所以对其他开发工具并不熟悉。期望可以由开源社区中熟悉相关编辑器/IDE的开发者参与贡献，这样效率更高一些。您可以查看 [更多炫酷彩虹屁](awesome-rainbow-fart.md) 页面，这里已经罗列了一些来自开源社区的优秀贡献。

## 如何修改内置语音包（增加/修改关键字等）

NOTE：不建议直接修改内置语音包的配置文件，因为当语音包版本更新时，会覆盖之前的所有修改。请遵循以下步骤进行修改：

1. 安装并启动插件
2. 点击 Web 界面中的 `打开语音包所在目录`。
3. 在该目录下复制内置语音包 `built-in-voice-chinese` 文件夹，修改为其他名称（例如：built-in-copy-01）。
4. 进入复制出的文件夹，修改 `manifest.json` 文件中的 `name` 字段，确保其与所在的文件夹的名称一致（例如：built-in-copy-01）。
5. 在 `contributes.json` 中，按自己的需求增加修改关键字或其他任意内容。
6. 在 Web 界面中点击 `刷新` 即可。

## 如何在 VSCode Remote 中使用？

连接远端服务器后，进入 VSCode 的扩展面板，找到 `@installed rainbow-fart`，VSCode 应该会提示你 `在 SSH:*.*.*.* 中安装 `，点击该按钮，安装成功后正常启动即可。

## 如何在 VSCode Remote 中修改内置语音包？

与本地修改大致相同，除了 `打开语音包所在目录` 并不可用，您需要自己定位内置语音包位置。在 CentOS 系统下，其目录大致为：`/$USER/.vscode-server/data/User/globalStorage/saekiraku.rainbow-fart/voice-packages/built-in-voice-chinese/`

## 能否不通过浏览器直接播放音频？

技术上可以，但是目前没有找到体积相对较小并且体验更好的解决方案。由于这是一个娱乐性质的插件，并不是实用性的。所以用户几乎不会为了这样的插件大动干戈（下载并配置额外依赖、忍受极大的扩展体积、等待漫长的下载时间等）。

## 能否更精确的检测关键字？

技术上可以，但是产品上没有这样实施的必要。理由同上，当用户的新鲜感过去之后，这个插件就几乎没有使用价值了，进行再多的技术迭代也就没有意义了。

## 插件的意义？为什么开发这个插件？

虽然上面说了这么多无意义，但如果从另外的角度和方式来说，其实还是有意义的。

1. 就插件的娱乐性质来说，我觉得还是比较成功的。至少有让一部分人在繁重、枯燥的工作中找寻到一点贴合自己工作和生活的沙雕式的快乐，对我来说足矣。在美剧《硅谷》中有一句经典的台词：“Make the world a better place”，为了实现这一点通常要付出极大的开发成本，而我只用到了简单又少量的代码，就传播了这样的快乐，简直可以说是“~~伟大的胜利~~” 😁。
2. 在之后可能会开发一个操作上简单方便的语音包生成器。这样，即便是不懂代码的 你的家人、子女、同学、跨部门同事、上级、男/女朋友等 也可以为你创建专属的语音包（或者作为某些节日的礼物赠送）。一旦它触及到了亲情、爱情、友情、回忆等主题，这件事的意义就不同了。对于一些看重这些属性的用户，上面所说的一切没有意义的事情，就开始变得有意义了。娱乐性插件也就变成了“实用性”插件了。
3. 其实最主要的还是为了测试一下自己开发的UI组件库（ http://qiqi-1996.github.io/qi-design-vue/#/index ），😂哈哈哈。