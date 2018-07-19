# friendly-computing-machine
* 关闭应用debug `APP_ENV=production, APP_DEBUG=false`
* 缓存配置信息 `php artisan config:cache`
* 缓存路由信息 `php artisan route:cache`
* 类映射加载优化 `php artisan optimize`
* 自动加载优化 `composer dumpautoload`
* 根据需要只加载必要的中间件 注释掉`app/Http/Kernel.php`里不必要的中间件
* 数据库配置文件加上长连接、取消模拟 `config/database.php`里加上
```
'options' => [
    PDO::ATTR_EMULATE_PREPARES => false, 
    PDO::ATTR_PERSISTENT => true
]
```
* 使用即时编译器（`JIT`），如：`HHVM、OPcache`
* 使用 `PHP 7.x`
* 使用代码缓存器`apcu`扩展
