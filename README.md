# MaterialDesignTheme
MaterialDesignTheme的入门篇
一、关于Material Design
从Android5.0开始引入的，是一种全新的设计语言（翻译为“原材料设计”），其实是谷歌提倡的一种设计风格、理念、原则。
拟物设计和扁平化设计一种结合体验。还吸取了最新一些科技理念。

1. 对于美工：遵循MD的界面设计、图标合集。
2. 对于产品经理：遵循MD界面设计、页面的跳转及动画效果、交互设计。
3. 对于开发人员：参与原型设计、辅助美工原型设计的素材准备。

二、MD的使用及开发

1. Google开放以及收集了一些最新的开源的项目(很多是自己开发的)，汇集到最新的support兼容支持包以及最新的5.X API里面
2. android-support-v4:最低兼容到Android 1.6系统，里面有类似ViewPager等控件
3. android-support-v7:appcompat、CardView、gridlayout、mediarouter、palette、preference、recyclerView(最低兼容到3.0)最低兼容到Android 2.1的系统，这个工程可以让开发人员统一开发标准，在任何的系统版本下保证兼容性。
4.现在一般做开发都是最低兼容到4.0。

##接下来我们来写一个使用MatrialDesign样式

	<!--
        Base application theme, dependent on API level. This theme is replaced
        by AppBaseTheme from res/values-vXX/styles.xml on newer devices.
    -->
    <style name="AppBaseTheme" parent="Theme.AppCompat.Light">
        <!--
            Theme customizations available in newer API levels can go in
            res/values-vXX/styles.xml, while customizations related to
            backward-compatibility can go here.
        -->
    </style>
    <!-- Application theme. -->
    <style name="AppTheme" parent="AppBaseTheme">
        <!-- All customizations that are NOT specific to a particular API-level can go here. -->
        <item name="android:textColor">@color/mytextcolor</item>
        <item name="colorPrimary">@color/colorPrimary_pink</item>
        <item name="colorPrimaryDark">@color/colorPrimary_pinkDark</item>
        <item name="android:windowBackground">@color/background</item>
	<item name="colorAccent">@color/accent_material_dark</item>
    </style>

相应的属性介绍

	colorPrimary：主色，如果你不手动自己去修改toolbar背景色的话，它就是默认的toolbar背景色
	colorPrimaryDark：主色--深色，一般可以用于状态栏颜色、底部导航栏
	colorAccent：（代表各个控件的基调颜色--CheckBox、RadioButton、ProgressBar等等）
	
![image](https://github.com/AndLollipop/MaterialDesignTheme/blob/master/images/design.png)





