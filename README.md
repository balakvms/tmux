# tmux

# How to configure tmux


**A tmux** is a terminal multiplexer. It lets you switch easily between several programs in one terminal, detach them (they keep running in the background) and reattach them to a different terminal.

## https://github.com/tmux/

### Create .tmux.conf under $HOME directory

1. ***Mouse mode is on***

```
set -g mouse on
```

2. ***Reconfigure prefix Ctrl-B to Ctrl-X, for each access***

```
set-option -g prefix C-x
unbind-key C-a
bind-key C-a send-prefix
```

3. ***Set easier window split keys***

```
bind-key v split-window -h
bind-key h split-window -v
```
4. ***For easy config reload***

```
bind-key r source-file ~/.tmux.conf \; display-message "~/.tmux.conf reloaded."
```



