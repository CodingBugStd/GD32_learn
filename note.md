# arm gcc工具链编译

## 使用Embedded IDE插件

从arm官网下载工具链，设置插件中的工具链路径。

通过EIDE插件新建一个空项目，选择cortex-m项目，加入相关源文件。

设置工作区

- cpu类型
- 芯片名称
- 链接脚本
- 设置构建器
- ......

## 链接脚本&启动文件

链接脚本可以根据STCubeMX生成ST芯片的gcc工程的链接脚本更改，启动文件同理。

## 烧录配置

基本上都是使用openOCD，openOCD的芯片配置可以使用ST的平替，接口配置选cmsis-dap(看具体仿真器)。

## 调试

使用cortex-m debug插件，使用openOCD的话需要去插件中指定openOCD的路径，还需要指定gcc工具链的路径。

在配置烧录设置的时候会在工作区的launch.json中会有一个对应的"openocd"的配置，调试时启动选openocd就能对接vscode了，没有必要使用gbd命令。

