我们添加了端到端测试来验证事件处理器的正常工作。

模拟测试的流程如下：

1. 网页加载后我们验证主图片被默认设置成第一个手机图片。

2. 我们模拟随机点击一副缩略图(代码中是第3张),验证此时主图替换为我们选择的那张缩略图。