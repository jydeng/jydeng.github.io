---
title: 解决prettier与eslint的冲突问题
date: 2018-09-18 13:04:01
tags:
---

## 起因

最近挖新坑，技术选择了 vue.js 全家桶 + elementUI， 代码风格统一选择了 eslint+prettier。prettier 自动格式化与 eslint 规则间有一些冲突需要解决，此间还涉及到 vuter 与 VSCode 的一些配置修改，牵涉较多，且网上也没有找到很准确的答案，特别记录一下。

## 现象

![](/images/2018091801.png)
如上图所示，基本就是提示行首多出空格，经过一段 google+baidu+bing.... 发现是 eslint 的 indent 规则导致的，因为规定是两个空格，而默认代码格式化会替 style、script、这类标签内的代码加上两个空格，2+2=4 故出错。

## 解决方案

1. 禁用 indent 规则，简单粗暴可行
2. 修改格式化规则，默认 style、script 不增加空格，推荐！

## 修改格式化规则

这一部分规则应该和 VSCode 有关系，故直接查找 VSCode 的配置

![](/images/2018091802.png)

找了一圈发现和 vuter 有关，Style Initial Indent 这一栏打钩去掉就可以了，再格式化一次应该没有问题了，script 也类似处理。

## 总结

多运用搜索引擎与 VSCode 的配置搜索，多折腾总能搞定，get it.

## 备份配置

最后备份一下我的配置。

### 插件

1. vuter
2. prettire
3. eslint

### VSCode 用户配置

```
{
  "terminal.integrated.shell.windows": "C:\\windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
  "eslint.autoFixOnSave": true,
  "eslint.validate": ["javascript", "javascriptreact", "html", "vue"],
  "eslint.options": {
    "plugins": ["html", "vue"]
  },
  "editor.tabSize": 2,
  "editor.formatOnPaste": true,
  "editor.formatOnSave": true,
  "editor.cursorStyle": "underline",
  "workbench.iconTheme": "vscode-great-icons",
  "workbench.colorTheme": "Visual Studio Dark",
  "vetur.format.defaultFormatter.html": "js-beautify-html",
  "git.autofetch": true,
  "git.enableSmartCommit": true,
  "prettier.stylelintIntegration": true
}
```
