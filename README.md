# AutoAlignButton

![image](http://og1yl0w9z.bkt.clouddn.com/17-6-30/11846761.jpg)

![](https://img.shields.io/badge/platform-iOS-red.svg) 
![](https://img.shields.io/badge/language-Objective--C-orange.svg) 
![](https://img.shields.io/badge/download-791K-brightgreen.svg)
[![CocoaPods](http://img.shields.io/cocoapods/v/AutoAlignButtonTools.svg?style=flat)](http://cocoapods.org/pods/AutoAlignButtonTools)&nbsp;
![](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg) 
[![Build Status](https://travis-ci.org/ReverseScale/AutoAlignButton.svg?branch=master)](https://travis-ci.org/ReverseScale/AutoAlignButton.svg?branch=master)

日常开发中对卡片布局需求很多，而 CollectionView 的量级又过重，就想着封装一份轻量级的卡片布局工具，基于 UIButton 后续又补上基于 UICollectionView 和 UILabel 的实现方式，支持图片、文字、自适应布局和手势等，使用安全方便。
（Swift 版：https://github.com/ReverseScale/AutoAlignButtonSwift）

AutoAlignButtonTools

| 名称 |1.多种实现列表页 |2.基于 Button 实现 |3.基于 Label 实现 |4.可编辑 collection 实现 |5.图文混合 Button 实现 |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 截图 | ![](http://og1yl0w9z.bkt.clouddn.com/17-8-28/24441803.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-8-28/17083630.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-8-28/8920945.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-8-28/38983256.jpg) | ![](http://og1yl0w9z.bkt.clouddn.com/17-8-28/66404166.jpg) |
| 描述 | 通过 storyboard 搭建基本框架 | 使用 UIButton+UIView 实现 | 基于 UILabel+UIView 实现 | 可编辑UICollectionView 实现 | 基于 UIButton+UIView 的图文混合实现 |

## Advantage 框架的优势
* 1.轻量化架构，文件少，代码简洁
* 2.不依赖任何其他第三方库
* 3.分离图文实现和文字按钮实现
* 4.支持SDWebImage或者YYWebImage的扩展
* 5.具备较高自定义性

## Requirements 要求
* iOS 7+
* Xcode 8+

## Installation 安装
### 1.手动安装:
`下载Demo后,将功能文件夹拖入到项目中, 导入头文件后开始使用。`
### 2.CocoaPods安装:
修改“Podfile”文件
```
pod 'AutoAlignButtonTools',:git => 'https://github.com/ReverseScale/AutoAlignButtonToolsCocoapodsDemo.git'
```
控制台执行 Pods 安装命令 （ 简化安装：pod install --no-repo-update ）
```
pod install
```
> 如果 pod search 发现不是最新版本，在终端执行pod setup命令更新本地spec镜像缓存，重新搜索就OK了

## Usage 使用方法
### AutoAlignButtonView 封装方法
#### 1.基本方法 
```objc
/*
* 是否九宫格 默认:打开
*/
@property (nonatomic, assign) BOOL isScratchableLatex;
/*
* 是：自动布局
*    countHorizonal 九宫格横排数量
*/
@property (nonatomic, assign) NSInteger countHorizonal;
/*
* 否：参数布局
*    buttonVerticalPadding 竖向间距
*    buttonHorizonalPadding 横向间距
*/
@property (nonatomic, assign) CGFloat buttonVerticalPadding;
@property (nonatomic, assign) CGFloat buttonHorizonalPadding;

```
#### 2.增强方法

```objc
/*
* 是否开启圆角 默认:关闭 打开后根据需要设置圆角参数（离屏渲染待优化）
*/
@property (nonatomic, assign) BOOL isCornerRadius;


// 数据源 （必选方法）
@property (nonatomic, copy) NSArray *dataTitleArray;
@property (nonatomic, copy) NSArray *dataImagesArray;

// 点击事件delegate
@property (nonatomic, weak) id<AutoAlignButtonViewDelegate> delegate;

```

使用简单、效率高效、进程安全~~~如果你有更好的建议,希望不吝赐教!
### 你的star是我持续更新的动力!


## License 许可证
AutoAlignButton 使用 MIT 许可证，详情见 LICENSE 文件。


## Contact 联系方式:
* WeChat : WhatsXie
* Email : ReverseScale@iCloud.com
* Blog : https://reversescale.github.io


