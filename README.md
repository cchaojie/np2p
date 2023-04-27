# np2p
P2P Distributed AI Computing Power For Painting

[示例](http://119.91.202.207:10083/3d/posture-editor.html)

通过将绘图任务分发给各个终端解决算力问题，本项目包含分发服务器[np2p-server](https://github.com/cchaojie/np2p-server)、客户终端程序[np2p-client](https://github.com/cchaojie/np2p-client)与超级融合应用[np2p-apps](https://github.com/cchaojie/np2p-apps)三个部分。

个人通过安装客户终端程序并连接分发服务器提供算力来赚钱。分发服务器提供用户最终的绘图服务界面，收取费用，给客户终端程序分成。

客户终端可以选择连接不同的分发服务器。分发服务器对客户终端的硬件评估分发任务。

一个典型的应用案例为：

用户需要渲染一个mov2mov视频。处理步骤如下：

1： 分发服务器：生成任务Id

2： 分发服务器：提取所有帧

3： 分发服务器：统一绘图参数

4： 分发服务器：分解任务

5： 分发服务器：根据客户终端状态分配客户终端执行任务

6： 客户终端程序：授收任务

7： 客户终端程序：完成并提交任务结果

8： 分发服务器：根据客户终端结果重新分配未完成任务

9： 分发服务器：确认所有客户终端完成任务

10： 分发服务器：合并所有帧生成最终视频
