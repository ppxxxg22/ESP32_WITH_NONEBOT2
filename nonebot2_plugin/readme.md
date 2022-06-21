> bot命令如下：
> > 帮助命令：
> >
> > `/esp32` 或 `/esp32 help`。
>
> > 查看已有开关命令：
> >
> > `/esp32 ls`。
>
> > 添加开关命令：
> >
> > `/esp32 add {开关名称} {开关地址}`。
> >
> > 其中，开关地址可以是`192.168.1.1`这种不带`http://`开头的地址，也可以是`http://192.168.1.1`这种带`http://`的地址，但不能是类似`http:192.168.1.1`这种写了，但又没完全写的地址。
>
> > 删除开关命令：
> >
> > `/esp32 del {开关别名}`。
>
> > 打开开关命令：
> >
> > `/esp32 on {开关别名}`。
>
> > 关闭开关命令：
> >
> > `/esp32 off {开关别名}`。
>
> > 自动变换开关：
> >
> > `/esp32 {开关名称}`。
> >
> > 本条命令会自动获取开关的当前状态并切换至下一状态。如当前开关为打开状态，则会自动切换至关闭状态，反之亦然。
>
> > 更改开关别名：
> >
> > `/esp32 rename {开关原名} {开关新名}`。
>
> > 更改开关地址。
> >
> > `/esp32 reurl {原地址} {新地址}`
> >
> > 其中新地址的填写要求同`/esp32 add`中的地址要求。
>
> > 更改配置信息（均为全局配置属性，一般情况下没什么用）：
> >
> > `/esp32 conf {配置名称} {参数}`
> >
> > > 可选的配置名称：
> > >
> > > + `on` -> 当发送`/esp32 on {开关名}`时，主机会访问`http://{开关地址}/on`这个路径，修改`on`这个键的值就是修改打开开关时访问路径。
> > >
> > > + `off` -> 同上。
> > >
> > > + `conf` -> 与上面两个类似，这是获取开关当前状态的链接子路径。
> > >
> > > + `timeout` -> 这个是访问链接的`timeout`的值。
> > >
> > > > 举例：
> > > >
> > > > `/esp32 conf on myon` 这条命令会将访问`http://{开关地址}/on`变为访问`http://{开关地址}/myon`。