# 常用的Promethues PromQL

## file system

** 1.文件系统使用报警 **
   
   ```
   (1- (node_filesystem_free_bytes{fstype=~"ext3|ext4|xfs"} / node_filesystem_size_bytes{fstype=~"ext3|ext4|xfs"}) ) * 100 > 90
   ```

** 2.磁盘写入速率

   ```
   sum by (instance,device) (irate(node_disk_bytes_written[2m])) / 1024 / 1024 > 50
   ```    

** 3.磁盘读取速率

   ```
   sum by (instance,device) (irate(node_disk_bytes_read[2m])) / 1024 / 1024 > 50
   ```

## 内存

** 1.内存使用 **
   
   ```
   node_memory_MemAvailable /1024/1024/1024 < 3
   ```

## 网络


## CPU

## 主机

1. 主机存活
   
   ```
   up == 0
   ```
