https://github.com/Assuner-Lee/LPDQuoteSystemImagesView
简书详细介绍：http://www.jianshu.com/p/2b9086d2c37b
# LPDQuoteSystemImagesView
(iOS-imagePicker仿qq仿微信--pickImage and quote)只需要几行简单的代码，就可以引入多选照片并引用照片的功能模块(贴上一个view，就获得了全部).  所有的功能都集成到了黑盒里，你需要做的只是初始化quoteview和取得quoteview 的已选择图片数组。（整个库包含必需资源只有270k，下载后请删除效果图和解压那个包含bundle的zip<包含一些小图标>）

这是贴上去的quoteView  (图片1)
![image](https://github.com/Assuner-Lee/LPDQuoteSystemImagesView/blob/master/效果图1.jpg)
这就是quoteView贴上去的效果，可以 点击可以选择或预览照片，点击右上角删除，可以通过引用这个view的selectedPhotos属性得到UIimage数组，保存或上传!


简单介绍下用法（目前）

1>.引入头文件

#import "LPDQuoteSystemImagesView.h"
2>.在一个controller类里， 初始化一个quoteSystemImagesView (UIview)

LPDQuoteSystemImagesView *quoteSystemImagesView =[[LPDQuoteSystemImagesView alloc] initWithFrame:CGRectMake(x, y, width, hight) withCountPerRowInView:5 cellMargin:12];
//初始化view的frame, view里每行cell个数， cell间距（上方的图片1 即为quoteSystemImagesView）

quoteSystemImagesView.maxSelectedCount = 6;
//最大可选照片数

quoteSystemImagesView.collectionView.scrollEnabled = NO;
//view可否滑动

quoteSystemImagesView.navcDelegate = self;    //self 至少是一个控制器。
//委托（委托controller弹出picker，且不用实现委托方法）

[Xview addSubview:quoteSystemImagesView];
//把view加到某一个视图上，就什么都不用管了！！！！

3>.获取引用图片

NSArray *imageArray = [NSArray arrayWithArray:quoteSystemImagesView.selectedPhotos];
//即可

////只需要贴上view，其他的在图库选照片，预览，保存，更新缩略图均不需要依赖新的对象参与，引入模块不需要额外代码，包括collect view ，一切处理响应都封在了quoteview及黑盒中。

效果图

图片2（选照片界面）

![image](https://github.com/Assuner-Lee/LPDQuoteSystemImagesView/blob/master/效果图2.PNG)


预览功能
3.预览

![image](https://github.com/Assuner-Lee/LPDQuoteSystemImagesView/blob/master/效果图3.PNG)
选中照片，蓝色框还有动画效果。。。。

其他：导航栏自动适应APP颜色，选中的视图排列可自由设置，删除带有动画效果，添加到最大数目没有➕，删除就出现。

最后感谢TZImagePickerController提供的一些源码！！

别忘了点个星星哦，谢谢大家！

https://github.com/Assuner-Lee/LPDQuoteSystemImagesView




