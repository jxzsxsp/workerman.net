# pidFile
## 说明:
```php
static Event Worker::$pidFile
```

此属性为全局静态属性，用来设置WorkerMan进程的pid文件路径。

这在监控中比较有用，例如将WorkerMan的pid文件放入固定的目录中，可以方便一些监控软件读取pid文件，从而监控WorkerMan进程状态。

如果不设置，WorkerMan默认会在```sys_get_temp_dir()```下自动生成一个pid文件，并且为了避免启动多个WorkerMan实例导致pid冲突，WorkerMan生成pid文件包含了WorkerMan文件的路径

如果无特殊需要，建议不要设置此属性


## 范例

```php
use WorkerMan\Worker;
Worker::$pidFile = '/var/run/workerman.pid';

$worker = new Worker('Text://0.0.0.0:8484');
$worker->onWorkerStart = function($worker)
{
    echo "Worker start";
};
```