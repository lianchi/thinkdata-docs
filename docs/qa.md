# 常见问题

## 问题 1: blabla `hahha`

blabla

```json
// manifest.json
{
    "name": "",
    "version": "",
    "contributes": [
    ]
}
```

## 问题 2:

balbal

<ImageZoom :src="URL_PREFIX+'/docs/assets/demo.jpg'" :border="true" width="300"/>

<Note>以下字段均为可选字段</Note>

### display-name <Badge>String</Badge>

`name` 字段更多的是语音包的标识ID，而 `display-name` 字段则可以在页面上显示绝大部分字符（空格、数字、Emoji 等）

### description <Badge>String</Badge>

语音包描述，可以写一些关于语音包的声明等纯文本。

### author <Badge>String</Badge>

作者名

### avatar <Badge>String</Badge>

头像图片，需要将图片文件拷贝到语音包目录中，然后在 `avatar` 字段中填写文件名。

<Note>部分内置语音包所使用的字段并未在此呈现，因为这些字段是实验性质的。</Note>
