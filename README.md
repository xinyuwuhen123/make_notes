### 阅读mockito代码:

#### 相关专业化名词:
- 假冒者：Imposter（ClassImposterizer）
- 实例化器：instantiator

###### 设置mock行为
该部分主要分为三个步骤：

mock.doSome(): 为mock方法设置OngoingStubbingImpl，并存放在ThreadLocal中。
执行when方法：执行when方法从mock对象的ThreadLocal中获得mock方法的桩对象OngoingStubbingImpl
设置mock行为。对OngoingStubbingImpl设置mock行为，如thenReturn、thenThrow等。
