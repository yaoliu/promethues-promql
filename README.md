# 常用的Promethues PromQL

## file system

1.文件系统使用报警
   
   ```
   (1- (node_filesystem_free_bytes{fstype=~"ext3|ext4|xfs"} / node_filesystem_size_bytes{fstype=~"ext3|ext4|xfs"}) ) * 100 > 90
   ```

1. 内存
   
   ```
   node_memory_MemAvailable /1024/1024/1024 < 3
   ```

## 网络


## CPU

## 内存

