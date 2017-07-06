记录一下自己所需的SublimeText 3技巧和工具

# 目录
<!-- MarkdownTOC -->

- [插件](#插件)
    - [插件管理](#插件管理)
    - [Markdown系列插件](#markdown系列插件)
        - [实时预览](#实时预览)
        - [Markdown Editing](#markdown-editing)
        - [MarkdownTOC](#markdowntoc)
    - [插件开发](#插件开发)

<!-- /MarkdownTOC -->

<a name="插件"></a>
# 插件

Sublime可以通过插件扩展功能。

<a name="插件管理"></a>
## 插件管理


<a name="markdown系列插件"></a>
## Markdown系列插件

<a name="实时预览"></a>
### 实时预览


<a name="markdown-editing"></a>
### Markdown Editing


<a name="markdowntoc"></a>
### MarkdownTOC

MarkdownTOC是Sublime Text 3下一款通过识别Markdown标题关键字来自动生成和维护目录的插件（[Reference](https://packagecontrol.io/packages/MarkdownTOC)）。
```
# Header 1
## Header 2
### Header 3
#### Header 4
```

#### 配置

默认的配置参数只会生成普通的目录结构，如需生成Github模式下带跳转的目录，可参考如下配置（[配置文件](https://github.com/PeryZen/SublimeText/blob/master/MarkdownTOC.sublime-settings)）：
```
{
    // 自动生成跳转链接
    "default_autoanchor": true,

    // Github相关配置项
    "default_autolink": true,
    "default_bracket": "round",
    "default_lowercase_only_ascii": true,

    // 三级目录结构
    "default_depth": 3,

    // true - non-ASCII characters in link ids are URL encoded. e.x. [中国的例子][%E4%B8%AD%E5%9B%BD%E7%9A%84%E4%BE%8B%E5%AD%90]
    // false - non-ASCII characters in link ids are not URL encoded. e.x. [中国的例子][中国的例子]
    "default_uri_encoding": false
}
```

#### 插入TOC

点击插入TOC操作`Tools > MarkdownTOC > Insert TOC`，会在Markdown文档头部生成MarkdownTOC目录。  
其中depth参数可以单独为特定文档设置目录层级，0表示无限层级，1，2，3...分别表示N级目录。
```
<!-- MarkdownTOC depth=3 -->

- [插件](#插件)
    - [管理插件](#管理插件)
    - [Markdown](#markdown)
        - [MarkdownTOC](#markdowntoc)

<!-- /MarkdownTOC -->
```

#### 更新TOC

保存文档或点击更新TOC操作`Tools > MarkdownTOC > Update TOC`会自动更新目录。

<a name="插件开发"></a>
## 插件开发


