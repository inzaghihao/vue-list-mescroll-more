# vue-list-mescroll-more
vue 下拉刷新上拉加载mescroll-more 插件tab页 demo

根据 http://www.mescroll.com/preview.html?name=list-mescroll-more 这个demo 改写成vue版

踩了一些坑，记录一下

1. 在切换每一个tab页面的时候初始化 创建MeScroll对象,内部已默认开启下拉刷新,自动执行up.callback,刷新列表数据;
2. 用配置 不用配置`clearEmptyId: clearEmptyId`,只需要配置 `warpId : clearEmptyId` ;
3. 更新列表数据 根据tab 的index 值做switch判断，首先要判断下拉刷新时 page.num ==1 ,清空当前tab内容数组数据，然后重新赋值
4. 静下心认真不急躁，多思考善于总结
