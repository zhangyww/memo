# linux资源和性能数据

## cpu
top可以用于查看当前系统的包括cpu、内存等的使用情况。

## 内存(memory)
查看内存使用量
```sh
free -h
```
查询的结果结构如下
```
              total        used        free      shared  buff/cache   available
Mem:           3.7G        134M        2.6G        532K        1.0G        3.3G
Swap:            0B          0B          0B
```
其中total列是总数(Mem或Swap的总数)；used是内存已使用量；buffers是内核的buffers使用量；cache是页缓存和slabs内存缓存的使用量；buff/cache是buffers和cache的总使用量。available是目前真正的可使用量。查询的结果都是对/proc/meminfo的统计。

## 磁盘(disk)
查看分区的磁盘使用量
```sh
df -h
```

查看文件或文件夹实际磁盘用量
```sh
# 查看当前目录的总磁盘占用
du -s .
```