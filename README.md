# 导出知乎收藏夹为markdown

批量将知乎收藏夹中的回答、文章、想法等内容导出为 Markdown 文件，并下载图片。

## 关于本项目

本项目是基于 [zanghuaren/ZhiHu-Collection-To-Markdown](https://github.com/zanghuaren/ZhiHu-Collection-To-Markdown) 的修改版本

## 更新日志

### 2025.5.14

1.将图片保存方式由链接改为本地保存。

2.增加了文件头部参数。

3.修改了排重机制，不再使用哈希值，而是通过文章url和最后修改时间排重。

4.优化代码结构，增强健壮性。

### 2025.4.10

**创建原项目分支**

1.新增批量下载收藏夹内容，读取url.json获取收藏夹链接及保存路径，以下载多个收藏夹内容。

2.新增验证文件重复功能，同名同哈希值文章将跳过下载。

3.修改文件命名规则。

## 使用方法

### 1.配置json

将自己的cookie放到"cookies.json"文件中。

打开知乎，F12，右键复制curl，然后去<https://curlconverter.com/> 转换到JSON格式。

注意json文件要用双引号。
示例：

```json
{
    "_zap": "根据实际获取的cookies填写，下同",
    "d_c0": "",
    "_xsrf": "",
    "q_c1": "",
    "edu_user_uuid": "",
    "Hm_lvt_98beee57fd2ef70ccdd5ca52b9740c49": "",
    "z_c0": "",
    "__zse_ck": "",
    "tst": "",
    "BEC": "",
    "SESSIONID": ""
}
```

### 2.配置收藏夹url及保存路径

将图片保存路径、收藏夹链接及markdown文件保存路径放到"url.json"文件中。
示例：

```json
{
    "global_image_path": "这里填图片文件保存路径",
    "collections": [
        {
            "url": "这里填收藏夹1链接",
            "path": "这里填md文件保存路径"
        },
        {
            "url":"这里填收藏夹2链接",
            "path":"这里填md文件保存路径"
        }
    ]
}
```
## 注意事项

**本项目仅供技术研究，用户需遵守相关协议及法规。下载内容不得用于商业用途，开发者不对滥用行为负责。**

