# kotlin-grammar

## kotlin中快速引用布局
  首先引入maven包：
  ```
  implementation group: 'org.jetbrains.kotlin', name: 'kotlin-android-extensions-runtime', version: '1.4.32'
  ```
  然后在plugins中启用kotlin-android-extensions:
  ```
  id 'kotlin-android-extensions'
  ```
  ***
  
## kotlin中内置函数let、also、with、run、apply
  Kotlin中有一些便于开发者编码的内置函数，能大大提高开发者的开发效率，下面我们来分开介绍。
  * let
     * 函数定义
        它是一个作用于函数
     * 函数作用
        1. 可以在一个特定的作用域内定义变量
        2. 避免写一些重复的判空语句
     * 应用场景
        1. 在一个特定作用域内统一使用变量，如统一判空处理
     * 函数返回值
        let函数的返回值为：函数显示return的值，如果函数未显示return，则为函数最后一行表达式的值
     * 示例
     ```
     // 作用1：使用it替代object对象去访问其公有的属性 & 方法
     // 作用域内的it即代表object
     object.let{
       it.todo()
     }
    // 作用2：判断object为null的操作
    object?.let{//表示object不为null的条件下，才会去执行let函数体
      it.todo()
    }
    ```
  
  * also
  * with
  * run
  * apply
