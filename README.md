# CopyBoard

一款像素画辅助软件，帮助用户从高清影像向像素风转绘

![image](https://github.com/KevinLEEEEEEE/CopyBoard/blob/master/design/design.jpg)

![image](https://github.com/KevinLEEEEEEE/CopyBoard/blob/master/design/output.jpg)

## 如何使用

1. 下载压缩包
2. 打开 "./dist" 文件夹
3. 打开 "index.html"
4. 注意请用火狐浏览器打开，chrome有跨域访问限制，会影响webworker调用

## 设计

### UI设计

### 需求模型

#### 5W

when：在路上，任何时间，任何季节，突发奇想而手头电脑没有工具链（ps，ai等大型工具和aseprite等像素化工具）
where：室内外，只要有便携式电脑，可能遇到非常低配或者性能不足的情况
who：需要表达简单概念的像素画爱好者，想尝试像素画的初学者
what：一张图片（或者兼容格式的文件，暂时不实现了）
why：一定要自动保存，要能够像实体拷贝台一样，能够非常自由地移动和调整画布和待拷贝内容

#### 1H

1. 将图片通过copyBoard面板插入，可以选择以多少像素为一块映射成像素风的图片
2. 用户可以自行调整参考图片和绘画图层的位置，所有的绘画操作仅限于画板，参考图上无法作画
3. 用户绘画是可以通过选色选区颜色，或通过效果调整面板调整效果
4. 最终可以导出作品为图片

## 提取功能

+ 铅笔（左键单击）
+ 橡皮（右键单击）
+ 油漆桶（左键双击）
+ 油漆桶清除（右键双击）
+ 取色器（图层工具栏）
+ 调色面板
+ ~~HSVA选色面板~~
+ ~~图层面板~~
+ 参考图一件像素化
+ 自动保存
+ 输出面板（可调整亮度、对比度、饱和度）
+ 绘图区：可缩放、可移动

## 用例

### 【用例名称】 绘图

### 【用例描述】

+ 画手设置初始画布大小
+ 画手通过拖拽的形式导入参考图
+ 画手可以调整参考图的大小，位置，透明度，层级，修改名称，也可锁定，取色或删除参考图，可进行像素化操作
+ 将多个参考图叠加与画布之下，可以在上面进行基础绘制和临摹，可以通过颜色面板调整画笔颜色
+ 之后可以导出图片并通过效果面板调整效果

名词列表 -> 软件类

+ ~~画手~~
+ 全局画板：dom，长，宽，缩放比
+ 绘制画布：dom，长，宽，透明度，是否锁定，绘制状态
+ 参考画布：dom，长，宽，透明度，是否锁定，像素化单位
+ 调色面板：dom，上一个颜色，当前颜色
+ 输出面板：dom，输出长，输出宽，亮度，对比度，饱和度，格式，背景色

属性映射

设置大小，拖拽导入，调整位置， 调整透明度，调整层级，修改名称，取色，选色，删除图层，像素化，
铅笔绘制，橡皮擦除，油漆桶，锁定，调整乱高度，调整对比度，调整饱和度，设置格式，设置背景色，
设置输出长宽，输出，自动保存，滚轮缩放

分配

+ 全局画板：
+ 绘制画布：
+ 参考画布：
+ 调色面板：
+ 输出面板：
