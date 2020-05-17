# 足够好用，FFloat

[![](https://gw.alicdn.com/tfs/TB10J77tNv1gK0jSZFFXXb0sXXa-720-353.png)](https://github.com/Fliggy-Mobile)

> **FWidget** 用心提供精致的组件，助您构建精美的应用。

你好开发者，来见识一下，这是由我们精心为你烘培🍩的全新组件，**F～～～Float**。

![](https://gw.alicdn.com/tfs/TB1DTbvGy_1gK0jSZFqXXcpaXXa-360-360.jpg)


**FFloat** 是由 **[【阿里巴巴-飞猪-FliggyMobile 技术团队】](https://github.com/Fliggy-Mobile)** 所开发维护的 **FWidget** 系列组件中的第 **5** 个成员。

正如我们的 **Slogan**：**"用心提供精致的组件，助您构建精美的应用。"** 

我们正在用心的尝试雕琢出一套好用的精美的组件，来帮助开发者们更易构建出 **Beautiful App**。

在过去的几周中，我们已经陆续向开源社区开放了 **4** 个精致的基础功能性组件，收到了来自开发者们投出的 [**333** 个 **Star**](https://github.com/Fliggy-Mobile)，非常感谢开发者们的认可和支持 🥰。

如今，我们迎来了 **FWidget** 的第 **5** 个成员， **FFloat** 。  

 **FFloat** 的诞生，来源于我们日常开发中一直棘手的 **浮动元素** 问题。
 
我们几乎很难计算出，在  **FFloat**  出现以前，当需要开发如下交互元素时，我们的焦虑能让我们喝掉几罐[可口可乐](https://www.coca-cola.com.cn/)🥤

![](https://gw.alicdn.com/tfs/TB1YErvGvb2gK0jSZK9XXaEgFXa-331-114.gif)

当然，就这个例子🌰而言，算是十分简单的 **浮动元素** 示例了。

 **FFloat**  的出现，将会让一切的难题都迎刃而解。现在，时间点将会分为两段， **FFloat出现前**  和  **FFloat出现后** 。
 
![](https://gw.alicdn.com/tfs/TB1za6OGET1gK0jSZFrXXcNCXXa-720-403.png)
 
 
 **FFloat**  在化简为繁方面是天生的好手。
 
 这得在益于我们在  **FFloat**  内部进行了大量繁琐的逻辑处理和计算，使得开发者在使用时，能够以最自然的，最简单的方式去 **还原创造** 。


![](https://gw.alicdn.com/tfs/TB1j5H_GuH2gK0jSZFEXXcqMpXa-720-922.png)
![](https://gw.alicdn.com/tfs/TB10qvQFrj1gK0jSZFOXXc7GpXa-964-1232.png)


# ✨ 特性

这是  **FFloat**  为开发者们带来的一些特性：

- 同时支持 **锚点模式** 和 **绝对模式** 双定位模式

- 够灵活，但简单的 **位置控制** 

- 支持配置 **背景遮罩** 

- 自带 **精美动效** ，能够根据位置关系智能调整

- 丰富的 **装饰三角** 配置

- 外层容器支持 **圆角、边框、渐变、阴影** 等诸多配置

- 便捷的**显示/隐藏控制**


![](https://gw.alicdn.com/tfs/TB1BBv0FUY1gK0jSZFCXXcwqXXa-225-225.jpg)


# 🛸 传送区

#### 🛸 [【传送门：FFloat Github 主页 - 感谢您的 Star 🌟】](https://github.com/Fliggy-Mobile/ffloat)

#### 📖 [【传送门：FFloat 文档】](https://pub.dev/documentation/ffloat/latest/ffloat/ffloat-library.html)

# 📍 基于锚点元素的位置控制

> 足够简单，足够有效

![](https://gw.alicdn.com/tfs/TB1GwD9FhD1gK0jSZFyXXciOVXa-464-140.gif)

```dart
FFloat(
  /// 浮动元素内容
  (setter) => createContent(),
  alignment: _alignment,
  margin: _margin

  /// 锚点元素
  anchor: buildAnchor(),
)
```

**FFloat** 不可思议的地方在于，开发者只需要通过 `anchor` 参数提供一个锚点， **FFloat**  就能知道如何在正确的地方显示 **浮动元素**。 

而且 **FFloat** 不会对原本的锚点元素及可见视图树结构产生任何不利影响，这很神奇吧！

对于所要展示的内容， **FFloat** 通过  **FloatBuilder** 函数来构建。开发者只需要在该函数中返回需要展示的浮动内容，剩下的事情， **FFloat**  会处理好。

此外，在 **FloatBuilder** 函数中，开发者能够通过函数的参数获取到刷新函数  **StateSetter** ，这样可以将刷新范围限制在浮动内容区域中，而不是去刷新整个页面区域。这对于构建一个精美丝滑的应用来说，至关重要。

```dart
FFloat(
  (setter){
    return FButton(text: _text, 
      onClick: (){

        /// 更新浮动内容
        setter((){
          updateText();
        })            
      });
  },
  ...
)
``` 

如果对浮动元素出现的位置不满意， **FFloat**  提供了 `alignment` 和 `margin` 参数，使开发者能够以难以置信的简单的方式调整浮动元素的位置，直到满意为止。


`alignment` 提供了十分全面的相对位置选项： 

|类型|说明|
|:--|:--|
|topLeft|在锚点元素【上方】，且【左边缘】与锚点元素对齐|
|topCenter|在锚点元素【上方】，且水平居中|
|topRight|在锚点元素【上方】，且【右边缘】与锚点元素对齐|
|bottomLeft|在锚点元素【下方】，且【左边缘】与锚点元素对齐|
|bottomCenter|在锚点元素【下方】，且水平居中|
|bottomRight|在锚点元素【下方】，且【右边缘】与锚点元素对齐|
|leftTop|在锚点元素【左侧】，且【上边缘】与锚点元素对齐|
|leftCenter|在锚点元素【左侧】，且垂直居中|
|leftBottom|在锚点元素【左侧】，且【下边缘】与锚点元素对齐|
|rightTop|在锚点元素【右侧】，且【上边缘】与锚点元素对齐|
|rightCenter|在锚点元素【右侧】，且垂直居中|
|rightBottom|在锚点元素【右侧】，且【下边缘】与锚点元素对齐|

在此基础上，`margin` 参数能够让开发者基于当前的相对位置关系，进一步微调浮动元素的偏移量。

在过去，要实现这一切，需要耗费开发者大量的精力去处理复杂的位置关系逻辑，编写不同的算法以确定浮动元素的最终位置。

而现在，一切就是这么简单😎。

# 📌 基于绝对坐标的位置控制

> 多一种模式，多一种可能

![](https://gw.alicdn.com/tfs/TB1gnz8GrH1gK0jSZFwXXc7aXXa-858-508.gif)

```dart
GestureDetector(
  onPanDown: (details) {
    FFloat(
      (setter) => createContent(),
      autoDismissDuration: Duration(milliseconds: 2000),
      alignment: _alignment,
      canTouchOutside: false,

      /// 通过绝对坐标配置浮动元素位置
      location: Offset(details.globalPosition.dx, details.globalPosition.dy),
    ).show(context); /// 显示
  },
  child: FSuper(...),
)
```

在一些情况下，我们的浮动元素不需要基于一个锚点出现，而是希望它出现在一个确定的位置。

如果开发者知道一个这样的位置的话，就可以使用 `location` 参数来设置 **FFloat** 的位置。

此时，开发者完全不需要将 **FFloat** 放到视图树中包裹任何的元素。这意味着开发者可以随时随地，在任何回调或者函数中创建一个浮动元素。

通过 `FFloat.show(context)` 和  `FFloat.dismiss()`，开发者可以随时轻松的控制浮动元素的 **显示/隐藏** 。

而 **FFloat** 的其它一切配置都依旧有效。

#  💫 背景遮罩及动效

> 将效果丰富，将实现简化

![](https://gw.alicdn.com/tfs/TB179P9GuH2gK0jSZFEXXcqMpXa-720-135.gif)

```dart

# 背景遮罩演示
FFloat(
  (_) => buildSearchWidget(),
  color: Colors.black.withOpacity(0.95),

  /// 配置背景遮罩颜色
  backgroundColor: Colors.black26,
  corner: FFloatCorner.all(20),
  margin: EdgeInsets.only(bottom: 10, left: 10),
  anchor: buildAnchor(),
  alignment: FFloatAlignment.topRight, 
 
  /// 配置点击非浮动元素区域是否隐藏
  canTouchOutside: false,
)
```

在  **FFloat**  中，只需通过 `backgroundColor` 一个参数，就能实现浮动元素出现时的背景遮罩效果。

默认情况下，当浮动元素出现时，会拦截所有事件，开发者可以通过 `canTouchOutside` 这一参数关闭该模式。

```
# 动效配置
FFloat(
  (_) => FSuper(text: "Surprise😃 !"),
  anchor: buildAnchor(),

  /// 当该参数不为 null 时，FFloat 会在指定时长后自动消失
  autoDismissDuration: Duration(milliseconds: 2000),

  /// 配置动效时长
  animDuration: Duration(milliseconds: 800),
),
```

 **FFloat**  自带精美的交互动效，根据浮动元素位置的不同，动效能够自动的进行调整，以呈现最优雅的视觉效果。

通过 `animDuration` 参数，开发者可以自行定义动效时长。当然，如果不需要任何动效，只需传入 `null` 即可。

在很多场景中，我们往往希望一个浮动元素出现后，能够在持续一段时间后自动消失。

通常，要实现这样的效果，开发者需要创建独立的计时器，以及状态机，在特殊的状况下，还需要额外的进行状态逻辑校验，以确保这一效果天衣无缝。需要考虑的逻辑实在太多。

而  **FFloat**  的出现，使得开发者只需通过 `autoDismissDuration` 参数，就能够实现这一功能。

# 🔺 装饰三角

> 省力，省心，省内存

![](https://gw.alicdn.com/tfs/TB1L3JoFEH1gK0jSZSyXXXtlpXa-753-220.gif)

```dart
FFloat(
  (setter) => buildContent(),
  anchor: buildAnchor(),

  /// 配置装饰三角的相对位置
  triangleAlignment: TriangleAlignment.start,

  /// 配置装饰三角的相对偏移量
  triangleOffset: Offset(10, 10),

  /// 配置装饰三角的宽
  triangleWidth: 20,

  /// 配置装饰三角的高
  triangleHeight: 15,
)
```

在  **FFloat**  出现之前， **Tooltips** 风格的浮动元素实现往往过于繁琐。

而真正难住开发者的却是浮动元素上的一个  **小三角** 😲。相信经验丰富的开发者一定知道这背后的心酸。

由于平台系统没有提供三角或带有三角的组件支持，开发者不得不在使用  **Canvas**  绘制或使用图片替代的方案中作出抉择。

前者灵活高效，但实现十分繁琐，这可不仅仅是在 **Canvas** 上 **draw** 个三角形那么简单，还需要考虑与真正的浮动元素的融合问题。

后者实现方便，但对于不同颜色，不同位置、不同尺寸的三角，开发者需要为它们配置多套图片，对的内存也会随时间逐步累加。考虑到开发成本和效率，开发者们往往都会选择这种实现方式。

现在，**FFloat** 彻底解决了这些问题，兼具高效与灵活，甚至比开发者们的期望更进一步。

在上面的  **Code** 演示中，展示了 **FFloat** 在小三角方面的常用配置，包括简单的相对位置关系、尺寸、及可微调的位置偏移。

从此，开发者可以清理应用程序中的所有类似图片资源了 👏。

除了解决过去的问题， **FFloat**  更进一步的能够根据浮动元素以及锚点元素的相对位置关系，自动调整自身的三角形到合理的位置。而这一过程，对于开发者而言是毫无感知的。


```dart
FFloat(
  (setter) => buildContent(),

  /// 配置是否隐藏装饰三角
  hideTriangle: true,
  anchor: buildAnchor(),
),
```

默认情况下，FFloat 会展示装饰三角。如果不需要，开发者只用配置 `hideTriangle: true`，就可以将它隐藏。

# 🔆 圆角 & 边框

> 虽然简单，但不简陋

![](https://gw.alicdn.com/tfs/TB1xbhyFqL7gK0jSZFBXXXZZpXa-670-241.gif)

```dart

FFloat(
  (setter) => buildContent(),
  anchor: buildAnchor(),
  alignment: FFloatAlignment.bottomLeft,
  hideTriangle: true,

  /// 加上圆角
  corner: FFloatCorner.all(6),

  /// 加上边框
  strokeColor: mainShadowColor,
  strokeWidth: 1.0,
)
```

在上面的例子 🌰 中，我们能够清晰的看到，一个漂亮的带边框的圆角浮层，构建起来如此的简单。

**FFloat** 提供了 **FWidget** 系列组件一脉相承的，简单的设置圆角的方式，仅仅通过一个简单的 `corner` 属性就能灵活的配置圆角。

与 `corner` 配套的 `cornerStyle` 属性，允许开发者随时切换圆角的风格（圆角 or 斜切角）。

对于 **FWidget** 的老用户而言，相信已经知道，我们为组件配置边框效果，仅仅需要通过 `strokeWidth` 和 `strokeColor` 这样两个简单的属性即可。

我们的初心始终是，帮助开发者更简单、更高效的构建出精美的应用。

# 🌔 渐变 & 阴影

> 要简洁，也要出彩

![](https://gw.alicdn.com/tfs/TB11GHPFrj1gK0jSZFuXXcrHpXa-414-179.gif)

```dart

FFloat(
  (setter) => buildContent(),
  anchor: buildAnchor(),
  hideTriangle: true,
  alignment: FFloatAlignment.bottomCenter,

  /// 配置渐变
  gradient: SweepGradient(
    colors: [
      Color(0xffE271C0),
      Color(0xffC671EB),
      Color(0xff7673F3),
      Color(0xff8BEBEF),
      Color(0xff93FCA8),
      Color(0xff94FC9D),
      Color(0xffEDF980),
      Color(0xffF0C479),
      Color(0xffE07E77),
    ],
  ),
  
  /// 添加阴影
  shadowColor: Colors.black38,
  shadowBlur: 3,
  shadowOffset: Offset(3, 2),
)
```

是的，**FFloat** 在兼具了诸多能力之后，仍然对渐变进行了支持。

仅仅是通过一个简单的 `gradient` 属性，开发者就能获得惊艳的渐变效果。

此外，作为一个现代化的组件，**FFloat** 当然会对阴影作出支持。

开发者只需要配置 `shadowColor` 参数就能获得一个基础的阴影效果。 

如果想要更进一步对阴影作出调整的，可以使用 `shadowBlur` 和 `shadowOffset` 参数来完成。

# 👏 更多的精彩


![](https://gw.alicdn.com/tfs/TB1NGfIFAL0gK0jSZFtXXXQCXXa-460-500.gif)


浮动元素的问题，就让 **FFloat** 来解决就好了，开发者只需要用心美化的应用就够了。


### [想要了解更多详细内容？请访问 **FFloat** 官方主页 (PS：别忘了投出一个你认可的 **Star** 哦 😘)。](https://github.com/Fliggy-Mobile/ffloat)


# 😃 如何使用？

在项目 `pubspec.yaml` 文件中添加依赖：

## 🌐 pub 依赖方式

```
dependencies:
  ffloat: ^<版本号>
```

> ⚠️ 注意，请到 [**pub**](https://pub.dev/packages/ffloat) 获取 **FFloat** 最新版本号

## 🖥 git 依赖方式

```
dependencies:
  ffloat:
    git:
      url: 'git@github.com:Fliggy-Mobile/ffloat.git'
      ref: '<分支号 或 tag>'
```

> ⚠️ 注意，分支号 或 tag 请以 [**FFloat**](https://github.com/Fliggy-Mobile/ffloat) 官方项目为准。


[![](https://gw.alicdn.com/tfs/TB1NPD0FHH1gK0jSZFwXXc7aXXa-294-220.jpg)](https://github.com/Fliggy-Mobile/ffloat)

#### [感觉还不错？请到 《FFloat》的 Github 主页投出您认可的一个 Star 🌟 吧！](https://github.com/Fliggy-Mobile/ffloat)

# 往期组件

- [《FSuper》- 帮助开发者快速构建精美的复杂视图](https://github.com/Fliggy-Mobile/fsuper)

- [《FButton》- 为开发者准备了诸多美妙的配置项](https://github.com/Fliggy-Mobile/fbutton)

- [《FSwitch》- 具有优良交互和视效的精美开关元素](https://github.com/Fliggy-Mobile/fswitch)

- [《FRadio》- 一个适用于几乎任意单选场景的单选组件](https://github.com/Fliggy-Mobile/fradio)


