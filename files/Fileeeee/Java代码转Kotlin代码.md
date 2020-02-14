## Java代码转Kotlin代码

不会写Kotlin代码怎么办？使用 Android Studio(或IDEA) 把Java代码转为Kotlin代码

- **方法1** 
  **快捷键 ：Ctrl+Shift+Alt+K**

  **选中文件或代码，再按快捷键**

- **方法2** 
  **工具栏Code ->Convert Java File To Kotlin File**

- **方法3** 
  **选中文件 -> 右键 -> Convert Java File To Kotlin File**

  

根据提示操作

转换成Kotlin代码以后，基本上就可以使用了

再根据ide的提示，修改个别有错误的地方即可

常见错误由Kotlin的空安全造成，可添加？以允许空参数



ps.

编译Kotlin需要添加**Kotlin编译支持**，即在 build.gradle(project)下添加classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"

或者当弹出提醒 “You will have to configure Kotlin in project before performing a conversion”

点击 "Ok,configure Kotlin in the project"

它就会自动添加