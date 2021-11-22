# rn-food-collection-app
Udemy 课程 https://www.udemy.com/course/react-native-the-practical-guide/ 学习记录

## 第6章第6节

react 在原生应用中的导航和 react web完全不同。原生应用没有URL，用户不会在你的应用程序中输入URL。使用第三方库`react-navigation`来导航。

## 第6章第14节

`push` 和 `navigate`的区别：
如果已经在`CategoryMeals`页面，'navigate'什么也不会发生，`push`可以一次又一次的切换到同一个screen。它被一次又一次地推入同一个堆栈。

`push`的使用场景：
如果你在一个文件夹中，你想转到另一个文件夹，每个文件夹在技术上都是相同的文件夹screen，只是加载了不同的内容。在这种情况下，你可能想从a文件夹转到b文件夹，它使用相同的组件，相同的screen，在这种情况下可以使用`push`来推送新内容。

```js
props.navigation.navigate({routeName: 'CategoryMeals'}); //
props.navigation.push('CategoryMeals'); // 
```

`replace`方法并没有播放跳转动画，而是立即跳转到那里，你也没有自动返回按钮。因为堆栈是空的。
`replace`使用场景：在登录的时候，用户一旦已经登录不应该回到登录界面。那么可以简单的将登录screen替换为用户已登录的screen。如果你想回去，那么什么也不会发生，因为你回不去了。

`goBack`和`pop`:

goBack - close active screen and move back in the stack

pop - go back in the stack