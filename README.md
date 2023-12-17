# Script-to-launch-mutiple-terminal-of-terminator

Step 1: Create the necessary directory and an empty configuration file

```
mkdir -p ~/.config/terminator/
touch ~/.config/terminator/config
nano ~/.config/terminator/config
```

Step 2: Copy-Paste the following code(Make sure to adjust the display resolution as per your computer
```
[global_config]
  title_hide_sizetext = True
  enabled_plugins = LaunchpadCodeURLHandler, APTURLHandler, LaunchpadBugURLHandler
  suppress_multiple_term_dialog = True
[keybindings]
[profiles]
  [[default]]
    cursor_blink = False
    font = DejaVu Sans Mono 9
    scrollback_infinite = True
[layouts]
  [[default]]

    [[[root]]]
      position = -4:0
      type = Window
      order = 0
      parent = ""
      size = 1870, 1020

    [[[grand]]]
      position = 536
      type = HPaned
      order = 0
      parent = root
    [[[left]]]
      position = 942
      type = VPaned
      order = 0
      parent = grand
    [[[right]]]
      position = 942
      type = VPaned
      order = 1
      parent = grand

    [[[terminal1]]]
      profile = default
      type = Terminal
      order = 0
      parent = left
    [[[terminal2]]]
      profile = default
      type = Terminal
      order = 1
      parent = left

    [[[terminal3]]]
      profile = default
      type = Terminal
      order = 1
      parent = right
      command = ""
    [[[terminal4]]]
      profile = default
      type = Terminal
      order = 0
      parent = right
[plugins]
```
