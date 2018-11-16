# AndroidHookStartActivity

## AMSHook

两行代码实现动态启动未注册的Activity。


1.application标签里配置一个壳Activity 
```   
        <activity android:name=".HostActivity" />
```

2.注册一下其中this为context
```
      AMSHookUtil.hookStartActivity(this);
```

3.以后就可以按照标准的Intent启动为那些未被注册的Activity。
```
                Intent intent = new Intent(MainActivity.this, OtherActivity.class);
                startActivity(intent);
```

原理详解：http://www.jianshu.com/p/2ad105f54d07


