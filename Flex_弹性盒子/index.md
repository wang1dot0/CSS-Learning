Ⅰ. Flex basic structure:
1. Axis
  - main axis
  - cross axis
2. Container
  - container(parent)
  - item (child)

Tips: flex layout includes 12 css Attributes. Each of parent and child has 6. Normally, we usually use 4 attributes, and each of them has 2.

Container:
1. container(parent)
  - justify-content: 设置子容器沿着主轴方向排列
    -- 位置排列
    | flex-start
    | flex-end
    | center
    -- 分布排列
    | space-around
    | space-between
  - align-items: 定义如何沿着交叉轴方向分配子容器的间距(多个子容器还是水平排列)
    -- 位置排列
    | flex-start 
    | flex-end
    | center
    -- 基线排列
    | baseline
    -- 拉伸排列
    | stretch

2. item (child)
  - flex: 控制子容器的伸缩比例
    -- 无值(none): 0 0 auto
    -- 单值 
    | flex-basis: 表示宽/高. 如 10em, 30px, auto, content
    | flex-grow: 无单位. 如 1, 2
    -- 两个值
    | flex-grow|flex-basis: 如 1 30px
    | flex-grow|flex-shink: 如 1 1, 2 2
    -- 三个值
    | flex-grow|flex-shink|flex-basis: 如 1 1 10%
  - align-self： 单独设置子容器如何在交叉轴排列
    -- 位置排列
    | flex-start
    | flex-end
    | center
    -- 基线排列
    | baseline
    -- 拉伸排列
    | stretch

Axis
- flex-direction: 决定主轴的方向
  | row: 向右
  | row-reverse: 向左
  | column: 向下
  | column-reverse: 向上

Ⅱ. Flex Advanced Concept
1. Container(parent)
  - flex-wrap: 设置换行方式
    | nowrap: 不换行
    | wrap: 换行
    | wrap-reverse: 反向换行
  - flex-flow: flex-direction + flex-wrap 轴向与换行组合，即子容器沿着哪个方向流动，流动到终点是否允许换行.
    | row nowrap: 表示主轴向右，不换行
    | ...
  - align-content: 子容器多行排列时，设置行与行之间的对齐方式
    -- 位置排列
    | flex-start
    | flex-end
    | center
    -- 分布排列
    | space-between
    | space-around
    -- 拉伸排列
    | stretch

2. item(child)
  - flex-basis: 表示不伸缩情况下子容器沿主轴方向的原始尺寸。10em, 120px, 20%等
  - flex-grow: 子容器弹性伸展的比例。
  - flex-shink: 子容器弹性收缩的比例。
  - order: 改变子容器的排列顺序，覆盖HTML代码中的顺序，默认值为0，可以为负数，数值越小越靠前

  Refer to: http://blog.csdn.net/magneto7/article/details/70854472
