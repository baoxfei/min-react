# react 的流程

## mounted

  1. createRoot.render
  2. sheduler 开始调度 创建一个更新的 lane
  3. 开始走创建的流程
  4. beginWork  **递的过程**
     1. diff diff的时候 复用同一节点 更新元素
     2. 生成一棵wipTree
  5. completeWork **归的过程**
     1. effectList
     2. updateQueue
  6. beforeMutation
     1. 执行dom变化的准备工作
  7. mutation
     1. 遍历effectList 执行dom变化
  8. layout
     1. 绘制

## updated

  1. setState scheduler 开始创建一个lane 开始调度

## 其次 hooks的创建

  1. useState

## jsx react/jsx-runtime  -》 运行时的垫片
