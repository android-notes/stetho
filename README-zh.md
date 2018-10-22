# Stetho 外传



基于 com.facebook.stetho:stetho:1.5.0。解决了只能查看Activity中view布局问题，现在可以查看所有window的布局，比如 dialog,popupwindow,toast,自己通过window manager添加的window


![gif](https://github.com/android-notes/stetho/blob/sequel/stetho.gif?raw=true)

## 使用
 
 
```groovy
compile 'com.wanjian.sequel:fb-stetho:1.5.0.1'

```



## 注意
由于fb-stetho和 [sak-autopilot](https://github.com/android-notes/SwissArmyKnife) 采用了相同的监听window创建逻辑，所以都存在一个WindowManagerGlobal类，如果同时使用了这两个依赖会导致编译失败，
这时可以使用 `compile 'com.wanjian.sequel:fb-stetho:1.5.0.2'`这个版本解决。`1.5.0.2`中移除了WindowManagerGlobal，通过反射获取WindowManagerGlobal对象

[参考  https://github.com/facebook/stetho](https://github.com/facebook/stetho)
