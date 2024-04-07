### 简介
开发中遇到需要在主线程开启多个线程去并行执行任务，并且主线程需要等待所有子线程执行完毕后再进行汇总的场景。使用 CountDownLatch 就可以优雅的解决这种情况
###  使用方法
将 1 个程序分为 n 个互相独立的可解决任务，并创建值为 n 的 CountDownLatch，每当一个任务完成时，都会在这个锁存器上调用 countDown，等待问题被解决的任务调用这个锁存器的 await，将自己拦住，知道锁存器计数结束

### 原理
