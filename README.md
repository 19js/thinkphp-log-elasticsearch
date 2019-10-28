thinkphp-log-elasticsearch
======================================
  将thinphp 5.1日志推送到elasticsearch

# 版本说明
# 使用
+ 在config/log.php里面配置
```$xslt
return [
    // 日志记录方式，内置 file socket 支持扩展
    'type'        => 'Elasticsearch',
    'host'        =>'http://127.0.0.1:9200/local/', //local为索引名称，可以根据自己的需要更换
    // 日志保存目录
    'path'        => '',
    // 日志记录级别
    'level'       => ['debug','info','notice','warning','error','critical','alert','emergency','sql'],
    // 单文件日志写入
    'single'      => false,
    // 独立日志级别
    'apart_level' => ['sql','error'],
    // 最大日志文件数量
    'max_files'   => 0,
    // 是否关闭日志写入
    'close'       => false,
    'json'	=>	true
];
```