# ThinkPHP 5.0

## 模型和关联

ThinkPHP5.0 的模型是一种**对象-关系映射**（Object/Relation	Mapping，简称 ORM ）的封装，并且提供了 简洁的 `ActiveRecord` 实现。一般来说，每个数据表会和一个“模型”对应。

> ORM 的基本特性就是表映射到记录，记录映射到对象，字段映射到对象属性。模型是一种对象化的操作 封装，而不是简单的 CURD 操作，简单的 CURD 操作直接使用 Db 类即可。



## 控制器

#### 空控制器

访问一个不存在的控制器，就会触发空控制器检查：

默认空控制器类配置参数：

```php
'empty_controller' => 'Error'
```

```php
<?php
namespace app\index\controller;
class Error
{
    public function _empty($method)
    {
        return '当前操作名：'.$method;
    }
}
```



#### 空操作

访问一个不存在的操作方法，就会触发空操作检查：

```php
public function _empty($method)
{
    return '当前操作名：'.$method;
}
```

