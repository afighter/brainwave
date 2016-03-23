# 关于NSOperationQueue
## Operation Queues
Operation Queues（NSOperationQueue）是Objective-C对象，作用非常像dispatch queue（分发队列）。定于要执行的任务然后加入队列，操作队列会处理这些任务的日程和执行。就像GCD,Operation Queue帮忙处理所有的线程管理任务，确保任务尽可能快速有效的在系统上执行。

## Dispatch Queues
Disaptch Queues基于C机制用于执行特定任务。一个Dispatch Queue分发队列执行任务既可以串行也可以并行，但总是以先进先出顺序。一个串行Dispatch Q ueue(分发队列)一个时间只能执行一个任务，在出对或者开始新任务前等待直到当前任务完成。相反，一个并行Dispatch Queue不用等待已经开始的任务终止，而是启动尽可能多得任务一起执行。


## Dispatch Sources
Dispatch sources是一种C机制用于处于异步的特定类型的系统事件。
Dispatch sources are a C-based mechanism for processing specific types of system events asynchronously. A dispatch source encapsulates information about a particular type of system event and submits a specific block object or function to a dispatch queue whenever that event occurs. You can use dispatch sources to monitor the following types of system events:

Timers
Signal handlers
Descriptor-related events
Process-related events
Mach port events
Custom events that you trigger