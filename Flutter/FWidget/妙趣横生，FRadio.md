# 妙趣横生，FRadio.md

[![](https://gw.alicdn.com/tfs/TB10J77tNv1gK0jSZFFXXb0sXXa-720-353.png)](https://github.com/Fliggy-Mobile)

> **FWidget** 用心提供精致的组件，助您构建精美的应用。

现在，快扔掉你手中还没蘸蕃茄酱的薯条 🍟。

把目光聚焦到这 👀。

有请来自由 **[【阿里巴巴-飞猪-FliggyMobile 技术团队】](https://github.com/Fliggy-Mobile)** 开发的 **FWidget** 的全新成员， **F..Radio**，闪——亮——登——场～ 🎉🎉🎉

**FRadio** 十分擅长于处理单选任务场景，这点你可以从它被赋予的名称可以看出。

但是开发者，如果你脑海中此时浮现的单选仅仅是类似以下这样的

![](https://gw.alicdn.com/tfs/TB1Zv8yFpP7gK0jSZFjXXc5aXXa-114-37.png)

那么请调整好坐姿，妙趣横生的 **FRadio** 将给你带来精美创造力的解放，这也许会让你受到些许的惊艳。但请尽快适应它。我们还有很多想要展示给你的～～料。

![](https://gw.alicdn.com/tfs/TB10lXuFqL7gK0jSZFBXXXZZpXa-1620-888.png)


# ✨ 特性

来看看 **FRadio** 是如何打破常规的？

- 精彩的交互动效

- 支持对圆角精准控制

- 美妙的渐变效果支持

- 简单但有效的多状态视图构建支持

- 难以想象的、灵活的可配置项

![](https://gw.alicdn.com/tfs/TB1BBv0FUY1gK0jSZFCXXcwqXXa-225-225.jpg)


# 🛸 传送区

#### 🛸 [【传送门：FRadio Github 主页 - 感谢您的 Star 🌟】](https://github.com/Fliggy-Mobile/fradio)

#### 📖 [【传送门：FRadio 文档】](https://pub.dev/documentation/fradio/latest/fradio/fradio-library.html)

# 🎭 必备基础款

> 虽是熟悉的味道，不过更胜一筹

![](https://gw.alicdn.com/tfs/TB1ZWJAFuH2gK0jSZFEXXcqMpXa-403-95.gif)

```dart
FRadio(
  value: 1,
  groupValue: groupValue,
  onChanged: (value) {
    setState(() {
      groupValue = value;
    });
  },
),
```

构建一个基础款的单选元素，像过去一样简单，但表现力却更胜以往。

# 📌 可用态和可取消模式

> 一切从简，但仍要与时俱进

![](https://gw.alicdn.com/tfs/TB1OkXyFuT2gK0jSZFvXXXnFXXa-403-111.gif)

很明显，如今的单选元素不再像过去一样简单了。

我们希望它能在启用与禁用之间随意切换，即使选中了也能取消选择。

没问题，**FRadio** 早已为开发者们准备好了这一切，但仍然保持着充分的简洁。你只需要通过 `enable` 和 `toggleable` 两个属性，就能实现对这一切的掌控。

# 🔆 间距 & 圆角 & 边框

> 用最少的代码，创造最丰富的效果

![](https://gw.alicdn.com/tfs/TB1ABtzFAL0gK0jSZFAXXcA9pXa-403-86.gif)

毫无疑问，**FRadio** 来源于现实的场景。对于处理单选场景任务，它真的很在行。

丰富但简单的配置，可以完成众多形态、色彩以及交互各异的单选视效。

# 🌈 渐变

> 善用渐变创造美

![](https://gw.alicdn.com/tfs/TB1ns0zFrr1gK0jSZFDXXb9yVXa-403-86.gif)

渐变的支持，使得 **FRadio** 可以为单选元素来一次超快的视觉升级。

我们对美的创造不应该被束缚。

# 🍭 装饰

> 多有趣一点，就能多抓眼球一点

![](https://gw.alicdn.com/tfs/TB1rZBCFrH1gK0jSZFwXXc7aXXa-405-130.gif)

人们常常会被有趣的事物所吸引。

**FRadio** 预留了灵活的装饰接口，允许你对 **"有趣"** 下个定义。

# 🎨 这是自定义呀！

> 限制？就是用来突破的

![](https://gw.alicdn.com/tfs/TB19WNzFEY1gK0jSZFMXXaWcVXa-391-318.gif)

如果你发现 **FRadio** 精心准备的基础样式配置无法满足你的奇思妙想。

没关系，**FRadio** 为你准备了足够大的 **大招** 🍾。

使用 `FRadio.custom()` 构造函数，你将能毫无限制的创造可能，其余的交互、状态切换放心交给 **FRadio**。

![](https://gw.alicdn.com/tfs/TB1QAXyFuT2gK0jSZFvXXXnFXXa-297-434.gif)

你看，所以从现在开始，能束缚住你的，也不过只有自己而已。


### [想要了解更多详细内容？请访问 **FRadio** 官方主页 (PS：别忘了投出一个你认可的 **Star** 哦 😘)。](https://github.com/Fliggy-Mobile/fradio)


# 😃 如何使用？

在项目 `pubspec.yaml` 文件中添加依赖：

## 🌐 pub 依赖方式

```
dependencies:
  fradio: ^<版本号>
```

> ⚠️ 注意，请到 [**pub**](https://pub.dev/packages/fradio) 获取 **FRadio** 最新版本号

## 🖥 git 依赖方式

```
dependencies:
  fradio:
    git:
      url: 'git@github.com:Fliggy-Mobile/fradio.git'
      ref: '<分支号 或 tag>'
```

> ⚠️ 注意，分支号 或 tag 请以 [**FRadio**](https://github.com/Fliggy-Mobile/fradio) 官方项目为准。


[![](https://gw.alicdn.com/tfs/TB1NPD0FHH1gK0jSZFwXXc7aXXa-294-220.jpg)](https://github.com/Fliggy-Mobile/fradio)

#### [感觉还不错？请到 《FRadio》的 Github 主页投出您认可的一个 Star 🌟 吧！](https://github.com/Fliggy-Mobile/fradio)

# 往期组件

- [《FSuper》- 帮助开发者快速构建精美的复杂视图](https://github.com/Fliggy-Mobile/fsuper)

- [《FButton》- 为开发者准备了诸多美妙的配置项](https://github.com/Fliggy-Mobile/fbutton)

- [《FSwicth》- 具有优良交互和视效的精美开关元素](https://github.com/Fliggy-Mobile/fswitch)


