### Tmux激活鼠标功能[引用](https://www.cnblogs.com/ruichenduo/articles/9447765.html)

#### Tmux版本: 1.8

1, 新建~/.tmux.conf，加入
``` txt
setw -g mouse-resize-pane on
setw -g mouse-select-pane on
setw -g mouse-select-window on
setw -g mode-mouse on
```

作用：

(1) 鼠标拖动panel分割线 
(2) 鼠标点击激活鼠标所在的panel
(3) 鼠标点击切换活动window
(4)开启鼠标支持(滚轮回显窗口内容，选取文本等）

2，然后在tmux里面按  Ctrl+b，:

（ctrl+b下冒号，进入命令模式）

3，输入source ~/.tmux.conf回车

4，复原设置： 删除~/.tmux.conf，执行tmux kill-server
