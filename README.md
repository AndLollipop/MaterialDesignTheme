# MaterialDesignTheme
MaterialDesignTheme的入门篇
一、关于Material Design
从Android5.0开始引入的，是一种全新的设计语言（翻译为“原材料设计”），其实是谷歌提倡的一种设计风格、理念、原则。
拟物设计和扁平化设计一种结合体验。还吸取了最新一些科技理念。
层次感：View Z轴

1.对于美工：遵循MD的界面设计、图标合集。
2.对于产品经理：遵循MD界面设计、页面的跳转及动画效果、交互设计。
3.对于开发人员：参与原型设计、辅助美工原型设计的素材准备。
开发实现MD的设计----界面、动画、转场动画等等。

二、MD的使用及开发
	谷歌开放以及收集了一些最新的开源的项目(很多是自己开发的)，汇集到最新的support兼容支持包以及最新的5.X API里面。
	（preference：设置页面，可以通过配置文件达到界面设计的效果。）
	1）android-support-v4:最低兼容到Android 1.6系统，里面有类似ViewPager等控件。
	2）android-support-v7:appcompat、CardView、gridlayout、mediarouter、
	palette、preference、recyclerView(最低兼容到3.0) 
	最低兼容到Android 2.1的系统，这个工程可以让开发人员统一开发标准，在任何的系统版本下保证兼容性。
	（比如：Theme,value,布局，新的控件，新的动画特效实现）
	所以现在ADT、AndrodStudio一般都会直接创建项目的时候就直接帮你新建或者引入了一个叫做appcompat的项目。
	（这里可能会碰到很多问题：1.自动导入的appcompat-v7项目自身就是报错的，什么原因？build的版本太低了,要么是SDK很新但是兼容包没有更新。
				  2.appcompat-v7好不容易没报错，但是项目报错，一看控制台：报appcompat里面的某个res/values/theme/xxx属性不存在 等等问题。
				  什么原因？因为你引入的是很新的appcompat-v7项目，它要求必须很高的版本编译，然而Eclipse很蛋疼，在引入该项目的主项目编译的时候也必须要达到这个很高的版本---直接使用最高版本编译）


现在一般做开发都是最低兼容到4.0。
SDK升级：API升级、兼容包的升级、工具升级。

--------------------------1.MaterialDesign控制项目全局样式-------------------------------
1.引入appcompat-v7项目（包括了android-support-v7-appcompat.jar和资源文件）
2.写自己的全局样式：
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
	colorPrimary：主色，
	colorPrimaryDark：主色--深色，一般可以用于状态栏颜色、底部导航栏
	colorAccent：（代表各个空间的基调颜色--CheckBox、RadioButton、ProgressBar等等）
	"android:textColor"：当前所有的文本颜色


最后附上一张图片

![image](https://github.com/AndLollipop/MaterialDesignTheme/blob/master/images/design.png)





