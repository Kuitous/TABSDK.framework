# TABSDK.framework

# 使用方法
1、在项目中导入JXYTAB.framework

2、创建几个viewcontroller

3、在AppDelegate.m  添加头文件#import <JXYTAB/JXYTAB.h>

4、在AppDelegate.m 添加你创建viewcontroller的头文件

5、在didFinishLaunchingWithOptions:添加如下代码



-(BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    
    self.window = [[UIWindow alloc] initWithFrame:[UIScreen mainScreen].bounds];
    
    self.window.backgroundColor = [UIColor whiteColor];
    
    JXYTABViewController *tabvc=[[JXYTABViewController alloc] init];
    
    /*
    tabbar底部不带文字
    
    [tabvc addVcWithPurefigure:[[oneViewController alloc] init]];
    
    [tabvc addVcWithPurefigure:[[twoViewController alloc] init]];
    
    */
    
    
    /*底部带文字*/
    
    [tabvc AddVcWithTopText:[[oneViewController alloc] init] VC_Top_title:@"第一个控制器" titleSelected_NO_Color:0x6E6E6E titleSelected_YES_Color:0xD1271F titleFont:[UIFont systemFontOfSize:10]];
    
    [tabvc AddVcWithTopText:[[twoViewController alloc] init] VC_Top_title:@"第二个控制器" titleSelected_NO_Color:0x6E6E6E titleSelected_YES_Color:0xD1271F titleFont:[UIFont systemFontOfSize:10]];

    self.window.rootViewController =tabvc;
    
    [self.window makeKeyAndVisible];
    
    return YES;
}


6、在Assets.xcassets添加图片资源

图片名称等于视图的类名：    

XXXXController（未选中状态）  

XXXXController-2（选中状态）

YYYYViewController(未选中状态)  

YYYYViewController-2（选中状态）

fanhui     （返回按钮，样式自己选）



