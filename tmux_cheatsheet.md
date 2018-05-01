TMUX CHEATSHEET
===============

Common commands
---------------
* tmux			      start new window
* tmux new -s myname	      start new window with session name
* tmux a  #  		      attach
* tmux a -t myname 	      attach to named 
* tmux ls 		      list sessions 
* tmux kill-session -t myname kill session 

Tmux control key
---------------
* Ctrl + b	default
* Ctrl + a	user defined
* Ck		Ctrl + key

Sessions
--------
* Ck + s	list sessions
* Ck + $	name session

Windows (tabs)
--------------
* Ck + c 	create window
* Ck + w	list windows
* Ck + n	next window
* Ck + p	previous window
* Ck + f	find window
* Ck + ,	name window
* Ck + &	kill window

Panes (splits) 
--------------
* Ck + %	vertical split
* Ck + "	horizontal split
* Ck + o	swap panes
* Ck + q	show pane numbers
* Ck + x	kill pane
* Ck + +	break pane into window (e.g. to select text by mouse to copy)
* Ck + -	restore pane from window
* Ck + ⍽ 	space - toggle between layouts
* Ck +  q 	Show pane numbers, when the numbers show up type the key to goto that pane
* Ck +  { 	Move the current pane left
* Ck +  } 	Move the current pane right
* Ck +  z 	toggle pane zoom


Moving between panes 
--------------------
* Ck + →	move to the right panel
* Ck + ←	move to the left panel
* Ck + ↑ 	move to the superior panel
* Ck + ↓   	move to the down panel
* Ck + l	move to the right panel
* Ck + h	move to the left panel
* Ck + k 	move to the superior panel
* Ck + j        move to the down panel
* Ck + ;	switch between panels

Resizing Panes
--------------
###via command
* resize-pane -D (Resizes the current pane down)
* resize-pane -U (Resizes the current pane upward)
* resize-pane -L (Resizes the current pane left)
* resize-pane -R (Resizes the current pane right)
* resize-pane -D 20 (Resizes the current pane down by 20 cells)
* resize-pane -U 20 (Resizes the current pane upward by 20 cells)
* resize-pane -L 20 (Resizes the current pane left by 20 cells)
* resize-pane -R 20 (Resizes the current pane right by 20 cells)
* resize-pane -t 2 20 (Resizes the pane with the id of 2 down by 20 cells)
* resize-pane -t -L 20 (Resizes the pane with the id of 2 left by 20 cells)

###via shortcut
* h[Ck + →]	move to the right panel
* h[Ck + ←]	move to the left panel
* h[Ck + ↑] 	move to the superior panel
* h[Ck + ↓]   	move to the down panel

Copy mode
---------
Pressing Ck + [ places us in Copy mode. We can then use our movement keys to move our cursor around the screen. By default, the arrow keys work. we set our configuration file to use Vim keys for moving between windows and resizing panes so we wouldn’t have to take our hands off the home row. tmux has a vi mode for working with the buffer as well. To enable it, add this line to .tmux.conf:

* setw -g mode-keys vi

With this option set, we can use h, j, k, and l to move around our buffer. To get out of Copy mode, we just press the ENTER key or the ESC key. 


Misc
----
* Ck + d	detach
* Ck + t	big clock
* Ck + ?	list shortcuts
* Ck + :	prompt

Configurations Options
----------------------
### Mouse support - set to on if you want to use the mouse
* setw -g mode-mouse off (will activate all the settings below)
* set -g mouse-select-pane off
* set -g mouse-resize-pane off
* set -g mouse-select-window off

### Set the default terminal mode to 256color mode
set -g default-terminal "screen-256color"

### enable activity alerts
setw -g monitor-activity on
set -g visual-activity on

### Center the window list
set -g status-justify centre

### Maximize and restore a pane
unbind Up bind Up new-window -d -n tmp \; swap-pane -s tmp.1 \; select-window -t tmp
unbind Down
bind Down last-window \; swap-pane -s tmp.1 \; kill-window -t tmp

