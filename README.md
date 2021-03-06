## ViewPagerIndicator

 一个简单好用的ViewPagerIndicator，提供了五种类型，采用在XML布局中定制颜色大小等参数，在JAVA代码中只需二行代码就能为viewpager添加酷炫效果，并且支持轮播图。

[![](https://jitpack.io/v/LinweiJ/ViewPagerIndicator.svg)](https://jitpack.io/#LinweiJ/ViewPagerIndicator)

![ViewPagerIndicator.gif](https://github.com/LinweiJ/ViewPagerIndicator/blob/master/screen_shot/ViewPagerIndicator.gif)

## 文档

- [English](https://github.com/LinweiJ/ViewPagerIndicator/blob/master/README_EN.md)
- [中文](https://github.com/LinweiJ/ViewPagerIndicator/blob/master/README.md)



## 如何使用它？

### 先在 project的build.gradle 添加:

```
allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}
```

### 然后在module的build.gradle 添加:

```
dependencies {
	        compile 'com.github.LinweiJ:ViewPagerIndicator:0.0.2'
	}
```

## 使用

1 . 将ViewPagerIndicator 添加到xml

```
<com.lwj.widget.viewpagerindicator.ViewPagerIndicator
				android:id="@+id/indicator_line"
				android:layout_width="match_parent"
				android:layout_height="50dp"
				android:background="#efefef"
				app:default_color="#cdcdcd"
				app:distance="800dp"
				app:distanceType="BY_LAYOUT"
				app:indicatorType="LINE"
				app:length="24dp"
				app:radius="8dp"
				app:selected_color="#FF23EEF5"
			/>
```

Properties:

- `app:selected_color`  
- `app:default_color`   (如果 indicatorType=CIRCLE_LINE  default_color 为指示器唯一颜色 ,selected_color 不起作用)
- `app:radius`  (点的大小,在indicatorType= CIRCLE_LINE 的情况下 radius 是点的高)
- `app:length`   (只作用在 indicatorType=CIRCLE_LINE 的情况下,为 指示器点的长度)
- `app:distance`    (只作用在 distanceType=BY_DISTANCE 的情况下)
- `app:num`
- `app:indicatorType` (LINE;  CIRCLE; CIRCLE_LINE; BEZIER;SPRING)

​        LINE：线 ; CIRCLE：圆点(默认) ; CIRCLE_LINE：圆角矩形;  BEZIER：弹性球 ; SPRING： 弹簧粘性球

- `app:distanceType` (BY_RADIUS; BY_DISTANCE ; BY_LAYOUT )

​       BY_RADIUS：3倍radius ; BY_DISTANCE ：定义固定距离 ;BY_LAYOUT ：根据layout_width均分得到距离

2 .  java 

```java
  mViewPagerIndicator = (ViewPagerIndicator) findViewById(R.id.viewPagerIndicator);
   
   //viewpager是固定页数, 传入viewpager即可
   mViewPagerIndicator.setViewPager(mViewpager);

   //viewpager是轮播图 ,如:总数为100000个 实际展示页为6个 
   //需要传入实际展示个数num
   mViewPagerIndicator.setViewPager(mViewpager,num);
   
```

3.更多

  可以参考 demo/ 示例

## License

```
Copyright 2017 LinWeiJia

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
## 底部

随手给颗星呗 ? (>_@)