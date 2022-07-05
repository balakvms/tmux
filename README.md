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
unbind-key C-x
set-option -g prefix C-x
bind-key C-x send-prefix
```
```
unbind                  --- unbinds whatever functionality C-x had (if any).
set -g prefix           --- line informs tmux that the prefix will now be C-x.
bind-key . send-prefix  --- allows Ctrl + x to perform the send-prefix command. The send-prefix command sends the prefix keystroke to a window.
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



