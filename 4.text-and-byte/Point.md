# 第4章文本和字节序列
## 重点
1. 编码和解码
2. bytes，bytearray对象各个元素是介于0-255之间的整数，切片始终是同一类型的二进制序列
3. 结构体和内存视图
4. memoryview类不是用于创建或存储字节序列的，而是共享内存，可以访问其他二进制序列
5. 编解码器
6. 处理文本文件
7. Unicode文本排序，对字符串来说，比较的是码位
8. os模块中的，编码函数fsencode(filename)，如果 filename 是 str 类型(此外还可能是 bytes 类型)，使用 sys.getfilesystemencoding() 返回的编解码器把 filename 编码成 字节序列;否则，返回未经修改的 filename 字节序列，fsdecode(filename)如果 filename 是 bytes 类型(此外还可能是 str 类型)，使用 sys.getfilesystemencoding() 返回的编解码器把 filename 解码成 字符串;否则，返回未经修改的 filename 字符串
9. 使用 surrogateescape 处理鬼符