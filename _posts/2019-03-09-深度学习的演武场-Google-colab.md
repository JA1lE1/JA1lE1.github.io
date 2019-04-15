---
layout:     post
title:      深度学习的演武场-co-lab
subtitle:   摆脱各种深度学习环境困扰
date:       2019-3-19
author:     JAYLEE
header-img: img/google-colab.png
catalog: true
tags:
    - 深度学习环境
    - Google产品
    - co-lab
---

# 深度学习的演武场-Goole-colab

![image title](https://img.shields.io/badge/auther-JA1LE1-orange.svg) ![image title](https://img.shields.io/badge/Weekly-Blog-brightgreen.svg)

## 写在前面（直接忽略:runner:）

- Anaconda给了我们很好管理深度学习有关的环境管理方法，但是有时候在处理各种环境问题时，依然有很多的地方令人抓狂，哎，世上无难事，只要肯放弃，所以我选择继续安装一个新的虚拟环境开始下一段深度瞎学之路🙈
- 没有服务器？一直在用windows，很多深度学习需要用linux，或者是mac，可是本弟弟只有一个弟弟级别的win10，怎么办？那就只能中国山东。。。。:stop_sign: **直接google-colab** 当然如果是因为**科学上网**等原因无法访问，这个就只能嗯~ o(*￣▽￣*)o
- 当然了，免费用GUP，TPU这么爽的事，我就不多说了 :clap:

## colab

- goole 给出了官方的[tutorial](https://colab.research.google.com/notebooks/welcome.ipynb)
  - 当然也是直接在colab中了

#### 初见colab

- colab好呀，真滴好:+1:
  - cuda安装
    - [参考初(知乎文章)](https://zhuanlan.zhihu.com/p/54389036) 见其终极篇
    - [直接到达](https://colab.research.google.com/drive/14OyDrmxzBmkJ8H51iodPE2aXHzCduKJP#scrollTo=bOHa-Sj8ywxn)
- 至于为什么安装，我想我要在co-lab上试一下github上rank不错的repo有关nlp pytorch的cs224n的一些实现，蛮不错的
  - ps.韩国人写的，yunjey也是韩国人，韩国人是真滴无孔不入在pytorch这个框框

#### 常见问题及解决方案

> 这里我主要分享一下我在使用google colab时遇到的一些问题和解决方案

1. **导入数据问题**（这里以导入kaggle比赛数据为例子）

   - 直接访问我在colab中的方法:point_right: [MY-Dataloader](https://colab.research.google.com/drive/19a-wzzNYI8berNQvxPwRZQ8O-fQDfuEj#scrollTo=JNLW0r69tC95)
   - 包括了获取google drive的权限方法
     - 这样就可以直接导入在google drive中的数据
   - 删除colab中有的sample_data
   - 通过kaggle api 下载到colab的disk中，注意这里每次使用需要重新下载
     - 我在colab中的解压方法只是一个示例，根据具体格式在具体解压

2. **import 自己写的moduel**

   - 这个其实google上蛮多方法的，但是下面这个方法比较切合实际，毕竟colab只是用来学习
     - from google.colab import files
       files.upload() 
     - 导入自己写好的.py文件就可以import自己的东西拉:100:

   