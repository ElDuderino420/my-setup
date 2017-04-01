# tmux

Install [powerline-status](https://powerline.readthedocs.io/en/latest/installation.html).

Create `~/.tmux.conf` with

    set -g @plugin 'tmux-plugins/tpm'new-session  

    set -g @plugin 'tmux-plugins/tmux-resurrect'
    set -g @plugin 'tmux-plugins/tmux-continuum'
    set -g @plugin 'tmux-plugins/tmux-sensible'
    set -g @plugin 'tmux-plugins/tmux-yank'
    set -g @plugin 'tmux-plugins/tmux-pain-control'

    set -g @resurrect-capture-pane-contents 'on'
    set -g @continuum-restore 'on'
    
    # Create a session if one doesn't exist (use with tmux a)
    new-session
    # Shift-click to drag-select; select/adjust panes with the mouse
    set -g mouse on
    # Word-movement keyboard keys work
    set-window-option -g xterm-keys on

    # Double-check this line
    source "~/.local/lib/python3.5/site-packages/powerline/bindings/tmux/powerline.conf"

    run '~/.tmux/plugins/tpm/tpm'
    
Install the [tmux plugins](https://github.com/tmux-plugins/tpm) with `Prefix + I`

TODO: Take a gander at https://github.com/tony/tmux-config/blob/master/.tmux.conf

## Using Resurrect and Continuum

TODO

## Keyboard reference

Prefix is `<ctrl>-b`

Keyboard  | Does
--------- | -----
c | New window
, | Rename window
% | Split vertical, todo use that other plugin
