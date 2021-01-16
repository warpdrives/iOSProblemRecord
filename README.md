# iOSProblemRecord

 1. iOS 自定义Present转场动画，Dismiss后黑屏
   [来源](https://www.jianshu.com/p/1a041dafa71d) <br/>
   问题修复：<br/>
    ```
    -(void)animateTransition:(id<UIViewControllerContextTransitioning>)transitionContext{ 
    ...
    
    if (fromVC.modalPresentationStyle == UIModalPresentationFullScreen) {
        [containerView addSubview:toVC.view];
    }
    ...
    
    }
    ```
    
 2. xcode 11.4 building for ios simulator, but the linked and embedded framework was built for ios
   [来源](https://stackoverflow.com/questions/63267897/building-for-ios-simulator-but-the-linked-framework-framework-was-built) <br/>
   问题修复：<br/>
    ```
    Under Build Settings - Navigate to Validate Workspace - Change it to YES (By Default its NO)
    
    ```


  
