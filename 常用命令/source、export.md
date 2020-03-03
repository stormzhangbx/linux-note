# source、export

[Linux 中执行Shell 脚本的方式（三种方法）](https://blog.csdn.net/xu380393916/article/details/80962561)

Shell 脚本的执行方式通常有如下三种：

- `sh test.py`
- `./test.py`
- `source test.py`

Shell可以类比Java、Python、JavaScript，是一门语言，它的执行都需要解释器。和Python、JavaScript一样，都有命令行交互模式和脚本模式。用户登录到Linux系统后，即进入Shell命令行交互模式。

运行shell脚本程序时，系统将创建一个子Shell。此时，系统中将有两个shell，一个是登录时系统启动的shell，另一 个是系统为运行脚本程序创建的shell。当一个脚本程序运行完毕，它的脚本shell将终止，可以返回到执行该脚本之前的shell。

## 1 source filename

表示不新建子Shell，直接在当前Shell中运行脚本

## 2 export var

用export定义的变量不仅对该Shell有效，对子Shell也有效

当我通过编辑/etc/profile文件来修改环境变量

/etc/profile

```sh
...
export PATH=...
```

`source /etc/profile`

source作用是在当前Shell中执行/etc/profile，而不是新建子Shell。用export定义PATH变量，使该变量对子Shell也有效。因为所有脚本模式中的子Shell都是登录Linux后进入的用户Shell的子Shell，综合source和export，上述修改可以使PATH变量在用户Shell和子Shell中生效。

