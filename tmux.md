set -g prefix C-w #

#up
bind-key k select-pane -U
#down
bind-key j select-pane -D
#left
bind-key h select-pane -L
#right
bind-key l select-pane -R

#copy-mode 将快捷键设置为vi 模式
setw -g mode-keys vi

set-option -g mouse on # 开启鼠标

#set -g default-terminal "screen-256color"
set -g default-terminal "tmux-256color"
