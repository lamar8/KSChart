# KSChart 效果图
<img src="https://github.com/saeipi/KSChart/blob/master/Resources/time.jpg" alt="分时图" width="600" height="464" align="middle"/>

<img src="https://github.com/saeipi/KSChart/blob/master/Resources/candle.jpg" alt="蜡烛图" width="600" height="464" align="middle"/>

<img src="https://github.com/saeipi/KSChart/blob/master/Resources/cross.jpg" alt="选中单个蜡烛图" width="600" height="464" align="middle"/>

### 500多条K线数据，真机示例内存占用为12.8M（其中KSChart占用4M左右），机型不同CPU占用差异会比较大，老设备在滑动时帧数会有所下降
<img src="https://github.com/saeipi/KSChart/blob/master/Resources/cpu.jpg" alt="cpu占用率" width="800" height="341" align="middle"/>

<img src="https://github.com/saeipi/KSChart/blob/master/Resources/memory.jpg" alt="memory占用率" width="800" height="459" align="middle"/>

### 如果觉得好用就打个赏呗
<img src="https://github.com/saeipi/KSChart/blob/master/Resources/Alipay.jpg" alt="Alipay" width="200" height="251" align="left"/>
<img src="https://github.com/saeipi/KSChart/blob/master/Resources/WeChatPay.jpeg" alt="WeChatPay" width="200" height="275" align="middle"/>

## 开发环境
- Xcode 11.0+
- Swift 5.1+

## 示例
请参考KSKChartView.swift
```swift
class KSKChartView: KSBaseView {
    
    var klineData = [KSChartItem]()
    var configure: KSChartConfigure = KSChartConfigure.init()
    
    weak var delegate: KSKChartViewDelegate?
    
    lazy var chartView: KSZeroChartView = {
        let chartView         = KSZeroChartView(frame: self.bounds)
        let style             = configure.loadConfigure()
        chartView.style       = style
        chartView.delegate    = self
        self.addSubview(chartView)
        return chartView
    }()
    ......
}
```
## Next Version
进一步优化CUP占用率（预计2020年4月底发布）

反馈/技术交流群:902071358
