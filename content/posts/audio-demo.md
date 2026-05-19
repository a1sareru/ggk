---
title: "音频功能演示"
date: 2024-01-15
draft: true
categories:
  - "听力"
tags:
  - "听力技巧"
  - "测试"
---

本文用于演示博客的音频 shortcode 功能，展示如何在文章中嵌入音频播放器。

## 示例 1：基本音频嵌入

以下是一个标准的音频播放器，使用有效的音频文件路径：

{{< audio src="audio/lesson1-greeting.mp3" >}}

这是通过 `{{</* audio src="audio/lesson1-greeting.mp3" */>}}` 语法插入的音频播放器。

## 示例 2：路径未指定时的错误处理

当 shortcode 未提供 `src` 参数时，将显示错误提示：

{{< audio >}}

上面应该显示一条错误提示信息，说明音频文件路径未指定。

## 示例 3：单篇文章中嵌入多个音频

一篇文章可以包含多个音频播放器，适用于对话练习或多段听力材料：

### 第一段对话

{{< audio src="audio/dialogue-part1.mp3" >}}

### 第二段对话

{{< audio src="audio/dialogue-part2.mp3" >}}

### 第三段对话

{{< audio src="audio/dialogue-part3.mp3" >}}

以上演示了在单篇文章中嵌入多个音频文件的能力。
