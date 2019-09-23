## 一、工程职责：

1、负责kafka相关的消息消费任务。

2、不对外提供服务能力，需要依赖于其他系统工程或者业务工程。

## 二、拆分原因：

1、单独拆除这个job工程是因为kafka相关的消费任务与普通的定时任务调度任务并不相同。

2、减少对kafka的依赖，如果柔和在一起，如果不想使用kafka处理任务，则需要删除一些配置和代码。

3、单一职责，每个服务都应该着力解决一个问题，而非很多个问题。职责比较清晰。