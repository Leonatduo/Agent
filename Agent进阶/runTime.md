runTime是指langchain中工具调用时自动注入的运行时上下文对象。可以获取当前会话的agentState和其它的全局上下文信息。

短期记忆: agentState, 我们可以自定义agentState类然后在创建模型的时候指定agentSchema， 然后在调用模型的时候通过tool中的runtime访问和修改agentState从而实现自定义的短期记忆存储。

长期记忆: store, 多用户共享，  是通过命名空间（通常是个元组） + key + value来实现的，  同样可以在tool中的runTime的get方法取到对应的记忆， 创建agent的时候也要加上对应的存储方式。
