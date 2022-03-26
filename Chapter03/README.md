# 第3章 探索 Linux 系统

## 本章命令

- ls => 列出目录内容
- file => 确定文件类型
- less => 查看文件内容

## 使用 ls 命令之乐

```bash
ls

ls /usr

ls ~ /usr

ls -l
```

### 选项与参数

- `command -options arguments`

```bash
# -t => 修改时间排序
ls -lt

# -r --reverse => 反向排序
ls -lt --reverse
```

**常用的 ls 命令选项**

| Option | Long Option      | Description        |
|--------|------------------|--------------------|
| -a     | --all            | 列出隐藏文件       |
| -A     | --almost-all     | 不列出`.`和`..`    |
| -d     | --directory      | `ls -ld`           |
| -F     | --classify       | 添加类型提示符     |
| -h     | --human-readable | 人类可读性`ls -lh` |
| -l     |                  | 长列表格式显示     |
| -r     | --reverse        | 反转（逆序）               |
| -S     |                  | 文件从大到小排序   |
| -t     |                  | 按修改日期排序     |

### 进一步了解长格式

- -rw-r--r-- => 文件类型与访问权限
- 属主 => 属组 => 其他人

## 使用 file 命令确定文件类型

- `file filename`
- 万物皆文件（everything is a file）

## 使用 less 命令查看文本文件

- `less filename`
- 配置文件 => 文本格式
- 脚本 => 文本格式
- ASCII => 美国信息交换标准码 => American Standard Code for Information Interchange => 电传打字机
- ASCII 文本 => 仅包含字符本身和少数基本的控制代码——回车符、制表符、换行符等

```bash
# 查看定义了系统中所有用户的文件
less /etc/passwd
```

**less 命令**

| Command | Operation      |
|---------|----------------|
| e       | 向前一行       |
| y       | 向后一行       |
| f       | 向前翻页       |
| b       | 向后翻页       |
| g       | 跳到第一行     |
| G       | 跳到最后一行   |
| /       | 搜索           |
| n       | 重复上一次搜素 |
| h       | 帮助           |
| q       | 退出           |

- less => 分页程序 => 替换早期 UNIX 的 more
- less is more => 少即是多
- less 可以前后翻页
- more 只能向前翻页

## 按图索骥

- Linux filesystem hierarchy standard => Linux 文件系统层次结构标准
- 鼠标 => 双击复制 => 单击中键粘贴
- 在 Linux 系统中，没有什么秘密可言

**Linux 系统中的目录**

| 目录           | 注释                         |
|----------------|------------------------------|
| /              | 根目录                       |
| /bin           | 二进制可执行文件             |
| /boot          | 内核、初始化 RAM、引导装载器 |
| /dev           | 包含设备节点的特殊目录       |
| /etc           | 包含系统范围的所有配置文件   |
| /home          | 存放用户主目录               |
| /lib           | 系统核心程序的共享库文件     |
| /lost+found    | 文件系统损坏的部分恢复       |
| /media         | 可移动存储设备的挂载点       |
| /mnt           | 手动挂载可移动存储设备       |
| /opt           | 安装软件（可选）             |
| /proc          | Linux 内核维护的虚拟文件系统 |
| /root          | 超级用户的主目录             |
| /sbin          | 二进制可执行文件（For root） |
| /tmp           | 临时文件                     |
| /usr           | 程序和支持文件               |
| /usr/bin       | 包含发行版安装的程序         |
| /usr/lib       | `/usr/bin`用到的共享库       |
| /usr/local     | 源码编译程序通常安装于此     |
| /usr/sbin      | 系统管理工具                 |
| /usr/share     | `/usr/bin`的共享数据         |
| /usr/share/doc | 存放软件包自带文档           |
| /var           | 存放动态数据                 |
| /var/log       | 日志文件、各种系统活动记录   |

## 符号链接

- 符号链接（软连接） => 一个文件被多个名称占用
- 解决版本升级问题
- 符号链接 -> 实际文件

## 硬链接

## 总结
