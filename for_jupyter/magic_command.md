# 打印环境信息
通常置于notebook的第一个cell，用于显示环境的信息。
- `-a "arun"`展示作者信息
- `-u -d -t`展示最后编辑的日期及时间戳
- `-m`展示机器的环境信息
- `-v`展示python的版本信息
- `-p numpy,pandas,matplotlib`展示python包的版本信息，注意多个包时逗号隔开中间不能有空格

```bash
%load_ext watermark
%watermark -a "arun" -u -d -t -m -v [-p numpy,pandas,matplotlib]
```