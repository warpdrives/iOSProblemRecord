# iOSProblemRecord

 1. iOS 自定义Present转场动画，Dismiss后黑屏
   [来源](https://www.jianshu.com/p/1a041dafa71d) <br/>
   问题修复：<br/>
   (```)
   fix:
   
    -(void)animateTransition:(id<UIViewControllerContextTransitioning>)transitionContext{
    ...
    
    if (fromVC.modalPresentationStyle == UIModalPresentationFullScreen) {
        [containerView addSubview:toVC.view];
    }
    
    ...
    
    }
    (```)
  
