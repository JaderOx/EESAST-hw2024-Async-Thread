# EESAST-hw2024-Async&Thread

作业共两道题，任选一道作答即可. 在提交的 PR 里需要注明作答了哪道题或者全部作答.

## 第 1 题

**作业要求:**

- 设计一系列异步计算结点，并进一步组织为一颗计算树；当数据结点发生变化的时候，与之关联的所有上级结点都将更新它们的输出.
- 打开 `HW-Async&Thread-1/` 下的 C# 项目，根据已有的代码编写完整程序. 可以根据自己的想法适当修改已有结构，也可以完全不遵循已有结构，使用如多线程等其他方案实现.
- 对计算的要求: 必须在数据变化之后立即开始 (即异步计算)，而不能在读取输出值时才开始 (即同步计算).
- 输出应当准确无误；或者，你也可以提供一个 `bool` 属性，指示输出值是否可以读取.

**拓展要求:**

在各结点的计算前加上延时，比如

```CS
val = ExprA.val + ExprB.val;
```

改成

```CS
Thread.Sleep(100);
val = ExprA.val + ExprB.val;
```

思考我们应当如何使用这些计算结点.

## 第 2 题