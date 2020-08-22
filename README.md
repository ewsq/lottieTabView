# lottieTabView [![](https://jitpack.io/v/wantWhat/lottieTabView.svg)](https://jitpack.io/#wantWhat/lottieTabView)
底部导航栏使用lottie动画

# 效果图
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190402103908540.GIF)
- 卡顿是因为录屏导致
- 基于[airbnb lottie-android](https://github.com/airbnb/lottie-android)的封装
- 动画资源在demo的assets目录下
# 使用
 - 根目录的build.gradle
```
allprojects {
    repositories {
        google()
        jcenter()
        maven { url 'https://jitpack.io' }
    }
}
```
- app 的build.gradle
```
dependencies {
    implementation 'com.github.wantWhat:lottieTabView:v1.0'
}
```
- xml中
```
 <LinearLayout
            android:id="@+id/tab_layout"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_gravity="bottom"
            android:background="@drawable/tab_bottom_bg"
            android:clipChildren="false"
            android:clipToPadding="false"
            android:gravity="bottom"
            android:orientation="horizontal">

            <com.chason.lottieview.LottieTabView
                android:id="@+id/tab_view_main"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                app:icon_normal="@drawable/ic_main_normal"
                app:lottie_path="mainpage.json"
                app:tab_name="首页"
                app:tab_selected="true"
                app:text_normal_color="@color/color66"
                app:text_selected_color="@color/colorMain"
                app:text_size="9sp" />

            <com.chason.lottieview.LottieTabView
                android:id="@+id/tab_view_deal"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginLeft="10dp"
                android:layout_weight="1"
                app:icon_normal="@drawable/ic_deal_normal"
                app:lottie_path="trade.json"
                app:tab_name="交易"
                app:tab_selected="false"
                app:text_normal_color="@color/color66"
                app:text_selected_color="@color/colorMain"
                app:text_size="9sp" />

            <ImageView
                android:id="@+id/main_add_btn"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginLeft="3dp"
                android:layout_marginBottom="22dp"
                android:layout_weight="1"
                android:scaleType="fitCenter"
                android:src="@drawable/ic_main_add" />

            <com.chason.lottieview.LottieTabView
                android:id="@+id/tab_view_msg"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_marginRight="10dp"
                android:layout_weight="1"
                app:icon_normal="@drawable/ic_msg_normal"
                app:lottie_path="news.json"
                app:tab_name="消息"
                app:tab_selected="false"
                app:text_normal_color="@color/color66"
                app:text_selected_color="@color/colorMain"
                app:text_size="9sp" />

            <com.chason.lottieview.LottieTabView
                android:id="@+id/tab_view_mine"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                app:icon_normal="@drawable/ic_mine_normal"
                app:lottie_path="user.json"
                app:tab_name="我的"
                app:tab_selected="false"
                app:text_normal_color="@color/color66"
                app:text_selected_color="@color/colorMain"
                app:text_size="9sp" />
        </LinearLayout>
```
