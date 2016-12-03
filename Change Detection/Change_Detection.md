#变化检测

![](/assets/change-detection.png)

变化检测是允许Angular保持我们的视图与我们的模型同步的过程。
变化检测在旧版本的Angular和新版本之间发生了很大的变化。在Angular 1中，框架保留了一长串观察者（每个属性绑定到我们的模板），需要检查每次一个摘要周期开始。这被称为脏检查，它是唯一可用的变化检测机制。
因为默认情况下Angular 1实现了双向数据绑定，改变的流程相当混乱，模型能够改变指令，指令能够改变模型，指令能够改变其他指令，模型能够改变其他模型。
在Angular 2中，信息流是单向的，即使使用ngModel来实现双向数据绑定，这只是单向流顶部的语法糖。在这个新版本的框架中，我们的代码负责更新模型。 Angular只负责通过选择的变化检测策略来反映组件和DOM中的那些变化。