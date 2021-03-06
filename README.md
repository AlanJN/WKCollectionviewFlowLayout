# WKCollectionViewFlowLayout 



## 要求

XCode6.0+, ios7.0+



## 使用效果

- 跨组交换带自动插入和删除

![cv.gif](跨组交换带自动插入删除.gif)

- 跨组交换 限定cell不能被交换

![](跨组交换限定.gif)

- 跨组交换

![](跨组交换.gif)

- 同组交换

![](同组交换.gif)

- 同组交换 限定cell不能被交换

![](同组交换限定.gif)

## **特点**

1. 功能

	**简介：实现了cell可拖动功能的flowlaout**
	
	- cell拖动范围自由定制（同组拖动，跨组拖动，某组不能拖动）
	- 可设置指定cell不可被拖动不可被交换
	- cell拖动到section中空白无cell处后自动插入(开关isAutoInsert，默认关闭)
	- cell拖动处collecitonview有效区域自动删除(开关 isAutoDelete,默认关闭)
	- 拖动cell时至屏幕需翻页且可翻页时自动滚动 
		
2. 高度监控

	- 利用代理模式，提供了一系列的方法实时监控Cell的布局位置和数据位置

## 安装方式

- 下载demo提取文件集成


- 现已加入cocoapods豪华午餐

```
platform :ios, '8.0'

target 'TargetName' do
pod 'WKCVMoveFlowLayout'
end
```

## 使用方式

1. 引入`WKCVMoveFlowLayout .h`
2. 新建`WKCVMoveFlowLayout`实例作为UICollectionView的Layout

```
WKCVMoveFlowLayout * flowLayout = [[WKCVMoveFlowLayout alloc] init];
[flowLayout setScrollDirection:UICollectionViewScrollDirectionVertical];
flowLayout.isAutoDelete = YES;//拖出区域自动删除
flowLayout.isAutoInsert = YES;//拖入尾部区域自动插入
UICollectionView   * collectionView = [[UICollectionView alloc] initWithFrame:CGRectMake(0, 0, 375, 667) collectionViewLayout:flowLayout];
```

## 联系方式

357863248@qq.com

[简书地址](http://www.jianshu.com/u/a492221b5126)