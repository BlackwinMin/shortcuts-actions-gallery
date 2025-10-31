# Move Desktop Items 全键盘调整桌面文件位置

[Shortcuts 示例动作下载](https://www.icloud.com/shortcuts/e695339c9f844469a437ad7cb356fc8e)

示例动作仅为向下移动，请参考 [Keyboard Maestro 版](https://github.com/BlackwinMin/Keyboard-Maestro-gallery/tree/master/Move%20Desktop%20Items)中的 AppleScript 脚本，自行修改座标参数以制作其他方向的动作。

以全键盘方式移动桌面上的文件，避免使用触控板或鼠标，可一次性移动整组文件。我经常在交通工具上办公，故设计此套动作。

Shortcuts 无法避免键位冲突，请根据实际情况自行设计快捷键。

不支持 Stack 布局。

使用前请根据您的实际情况修改座标增减量，可使用以下 AppleScript 脚本测量直面文件的位置，并算得纵横两个维度的插值。

```
tell application "Finder"
	set selectedItems to selection
	repeat with theItem in selectedItems
		get desktop position of theItem
	end repeat
end tell
```

出处：[《吭哧吭哧，全键盘调整 Finder 桌面文件位置》](https://utgd.net/article/21255/)。 

另有 [Keyboard Maestro 版](https://github.com/BlackwinMin/Keyboard-Maestro-gallery/tree/master/Move%20Desktop%20Items)。

![img](img.gif)