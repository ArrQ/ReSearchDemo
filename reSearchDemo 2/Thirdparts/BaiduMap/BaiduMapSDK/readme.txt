百度地图iOS SDK自v2.3.0起，采用可定制的形式为您提供开发包，当前开发包包含如下功能：
--------------------------------------------------------------------------------------
基础地图：包括基本矢量地图、卫星图、实时路况图和各种地图覆盖物，此外还包括各种与地图相关的操作和事件监听；
检索功能：包括POI检索，公交信息查询，路线规划，地理编码/反地理编码，在线建议查询，短串分享等；
定位功能：获取当前位置信息；
计算工具：包括测距（两点之间距离）、坐标转换、调起百度地图导航等功能；
--------------------------------------------------------------------------------------
当前版本为v2.5.0，较上一个版本（v2.4.1）的更新内容如下：

使用Xcode6创建工程时注意事项如下：在info.plist中添加：Bundle display name （Xcode6新建的项目没有此配置，若没有会造成manager start failed）【 新 增 】1. 新增对arm64 CPU架构的适配；基础地图1. 新增对iPhone6、iPhone6 plus的屏幕适配；定位功能1. 新增对iOS8定位的适配；在使用SDK为您提供的定位功能时，注意事项如下：需要在info.plist里添加（以下二选一，两个都添加默认使用NSLocationWhenInUseUsageDescription）：NSLocationWhenInUseUsageDescription  ，允许在前台使用时获取GPS的描述NSLocationAlwaysUsageDescription  ，允许永久使用GPS的描述【 修 复 】修复Tabber控制器中使用定位弹出框异常的问题；修复scrollenable=no，仍可以移动地图的问题；修复多边形在特定坐标下显示异常问题；修复定位时间戳错误的问题；修复autolayout时，BMKMapView横屏时无法自动扩展的问题；修复从B页返回到A页后，在A页的viewWillAppear方法中setCenterCoordinate无效的问题；