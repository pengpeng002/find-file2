# find-file2
软件采用c++的图形界面框架Qt开发，是一款基于NTFS文件系统的windows文件定位软件<br>
虽然是毕业设计，但我打算以后将这软件作为我主要的搜索软件，因此会不断进行优化和调整<br>
没有使用数据库的原因是考虑到一般用户电脑上都没装数据库，使用数据库的话，没装数据库的电脑就用不了，导致程序基本成为废物<br>
但现在感觉可以考虑写一个用数据库的，就给自己用就行了<br>
虽然程序的功能和设计基本全部来自everything，但也有一些改进之处<br>
一、提供了多语言选项，虽然没什么用<br>
二、对图片有更好的预览支持，可以进行缩放以及拖动。灵感来自以前和城建合作时做的项目有这一功能<br>
三、提供了查看文件属性框的功能，就是资源管理器里右键->属性弹出的框<br>
四、提供了限制搜索结果的选项，可以设置最大搜索结果数<br>
五、当有ntfs卷加入或移除时，点击重启即可获得该卷内容<br>
<br>
已知的程序的不足之处<br>
一、程序必须以管理员权限启动，因为为了搜索结果的正确性，程序启动时需要检查服务的运行状态。可以改，但这样就很难保证结果的正确性，进而导致需要重启程序<br>
二、程序搜索速度似乎不如everything，虽然也就慢一点点<br>
三、只支持UTF8与GBK编码，其余编码的文件在预览时均会乱码。不过正常来说，也没人用其他编码<br>
四、文件类型是用后缀名判断的，可能会有类型判断出错的情况。比如当用户乱改文件后缀名时<br>
五、搜索结果显示的信息只有文件名与路径。这个很好改，但因为我暂时用不到，所以一直没改。不过提供了查看属性框作为补偿<br>
六、在搜索结果数量过大时，会很慢。知道原因，但不太好改。因此提供了限制最大搜索数的选项，当然可以设置不做限制<br>
七、似乎在更新方面存在bug，这个不好说，只是我觉得有<br>
八、由于服务只是监听文件的更新。因此在程序长久未启动或者有大量的文件的新增或删除，更新文件应该会很大。没有遇到过，因为我大概三天两头就会启动一次
九、基于NTFS文件系统。如果不是NTFS文件系统的，就搜索不了。因此对可移动磁盘基本不行，因为可移动磁盘以FAT居多
