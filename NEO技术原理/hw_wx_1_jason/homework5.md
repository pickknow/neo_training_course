#### 描述交易的结构，生命周期

![image](https://i.postimg.cc/5yvptjj8/6.png)
![image](https://i.postimg.cc/Kcg0fpQ4/7.png)


#### 描述区块的结构，与生命周期

![image](https://i.postimg.cc/VLQDV9Hg/8.png)
![image](https://i.postimg.cc/hPLpWJkB/9.png)

#### 描述NEO是如何指定当前共识节点

> 当前投票选出下一轮公式节点，并且写入NextConsensus， 则当前节点由上一轮指定。

#### 对比 UTXO类型的交易，与合约交易的优劣

##### UTXO 
> 优点 只需要验证，无其他状态，无存储等，效率更高，编程简单

> 缺点  验证过程在某些时候过长

##### 合约交易 

> 优点 可编程，有状态，可存储， 验证速度快

> 缺点 复杂度， 安全性
