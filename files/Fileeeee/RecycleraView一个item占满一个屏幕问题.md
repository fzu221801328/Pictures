## RecycleraView一个item占满一个屏幕问题

#### 问题

问题如图1

![1](https://github.com/fzu221801328/Pictures/blob/master/files/recyclerview1.png?raw=true)

解决问题后如图2

![2](https://github.com/fzu221801328/Pictures/blob/master/files/recyclerview2.png?raw=true)



#### 修改item的布局

Recyclerview中显示的**item的布局**如下

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="horizontal"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <ImageView
        android:id="@+id/fruit_image"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        />

    <TextView
        android:id="@+id/fruit_name"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_gravity="center_vertical"
        android:layout_marginLeft="10dp"
        />

</LinearLayout>
```



看布局的android:layout_height

一开始我设置了ImageView和TextView的高为**wrap_content**，但是没有用

**原来是最外层布局LinearLayout的高为match_parent，将其改为wrap_content即可**

 