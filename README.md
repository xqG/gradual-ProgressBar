自定义带有渐变颜色的进度条
================
可以选择多种颜色,设置进度的背景色,
```Objective-C
- (void)initFlatRainbowProgressBar
{
    //设置背景色颜色
    self.progressBarFlatWithIndicator.backgroundColor = [UIColor redColor];
    
    //设置边框圆角大小
    self.progressBarFlatWithIndicator.layer.cornerRadius = 3;
    self.progressBarFlatWithIndicator.clipsToBounds = YES;
    //数组为渐变上有哪几种颜色
    NSArray *tintColors = @[[UIColor colorWithRed:255/255.0f green:186/255.0f blue:0/255.0f alpha:1.0f],
                            [UIColor colorWithRed:18/255.0f green:142/255.0f blue:183/255.0f alpha:1.0f],
                           ];
    _progressBarFlatWithIndicator.type               = YLProgressBarTypeFlat;
    //设置渐变颜色
    _progressBarFlatWithIndicator.progressTintColors = tintColors;
    //设置显示,隐藏进度条动画条纹
    _progressBarFlatWithIndicator.hideStripes        = NO;//(YES:隐藏,NO:显示)
}
```
