# Goldwave #

* 作者: Joseph Lee, NVDA contributors.
* 下载[稳定版][1]
* 下载[开发板][2]

一个提高音频编辑器 Goldwave 的可访问性和提供小贴士的插件。

## 快捷键 ##

* NvDA+Shift+C: 在音频编辑过程中切换命令。
* Control+Shift+P: 报告当前的轨道位置。
* NVDA+Shift+R: 报告当前编辑曲目的剩余时间。
* Control+NVDA+1: 报告您正在编辑的通道。
* Control+NVDA+2: 报告音频文件的总长度。
* Control+NvDA+3: 报告关于音频选择信息的摘要。
* Control+NVDA+4: 报告缩放级别。

关于Goldwave和键盘命令的更多信息，请参阅Goldwave手册。

注意: GoldWave 6需要64位版本的Windows 7或更高版本。 NVDA 2014.1或更高版本需要使用附加2.0。

## 版本17.05

* 增加了在启用调试日志记录的情况下运行NVDA时提供调试信息的功能,注意: 这需要（NVDA 2017.1或更高版本）。
* 更新翻译

## 版本16.12

* 版本方案现在是year.month而不是major.minor。

## 版本4.0

* 附加存储库已转移到GitHub（现在位于 https://github.com/josephsl/goldwave).
* 现在查找诸如通道名称,和其他状态信息之类的信息时性能得到改善。

## 版本3.0

* 增加了一条命令来报告当前曲目的剩余时间（NvDA + Shift + R）。
* 报告通道信息等状态信息时略有改进。

## 版本2.0

* 支持GoldWave 6，包括64位版本的GoldWave（请参阅上面的注释）。
* 现在可以从插件管理器（NVDA 2014.3及更高版本）访问附加组件帮助。
* 如果按左声道的Control + Shift + L等声道选择命令，NVDA现在会报告选定的声道。
* 数字编辑字段中的各种问题（如审查字段和混合对话框中的时间选择器）已得到修复，包括选择文本，更新值等。
* 当切换到其他程序时，命令通知设置将被记住。

## 版本1.2

* 修复了NVDA难以公布一些编辑字段的问题。
* 新增翻译
* 请注意，由于近期NVDA的变化，音频选择和其他状态命令在某些系统中可能无法按预期工作。

## 版本1.1

* 支持盲文中的消息通告。
* 音频选择摘要以英语以外的语言显示。
* 添加了更多命令通告，包括提示位置移动和删除/修剪操作。
* 修复了数字编辑字段中的问题，例如各种效果对话框中没有任何字段名称或错误字段名称被宣布。
* 新增翻译

## 版本1.0

* 发布初始版本。

[[!tag dev stable]]

[1]: https://addons.nvda-project.org/files/get.php?file=gwv

[2]: https://addons.nvda-project.org/files/get.php?file=gwv-dev
