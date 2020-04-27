# 常用的Promethues PromQL

## 磁盘

###1.磁盘使用报警
   
   ```
   (1- (node_filesystem_free_bytes{fstype=~"ext3|ext4|xfs"} / node_filesystem_size_bytes{fstype=~"ext3|ext4|xfs"}) ) * 100 > 90
   ```


