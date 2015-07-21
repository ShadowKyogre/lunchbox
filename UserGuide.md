A short guide to using the Lunchbox Window Manager

# Installation #

Download the latest tarball and extract it into a temporary folder.
Ensure you have development headers for the cairo graphics library and xcursor, as well as the X11 headers which both the cairo graphics library and xcursor depend upon.

From the commandline, traverse to the downloaded extracted files and run:
`make`

If this doesn't report any errors you can install it by running the following command as root:
`make install`
which simply copies the binary to `/usr/bin` and the theme files (text and images) to `/usr/local/share/lunchbox`

Once installed, the easiest way to run the window manager is by logging into a failsafe session (a plain X session with only an instance of xterm open) and simply running:
`lunchbox &`

You should immediately see a frame appear around your xterm session and a menubar appear at the bottom of the screen.  There is no launcher included with the window manager, so remember to open one otherwise you won't be able to do anything without switching back to the commandline.

If you want to quit lunchbox, send it the SIGINT signal and then trigger some kind of X event by clicking on the frame somewhere or running another program.

A commandline to do this would be:
`pkill -INT lunchbox && sleep 1 && xterm &`

The advantage of this is that windows will have had their EWMH state hints reset and won't all be minimized if you load another window manager. It opens another xterm instance to send lunchbox another X event to get it to wake up.

# Changing Programs #

Proceed to open some more programs from the command line.  If you normally run a GNOME desktop run:
`gnome-settings-daemon & nautilus & `

This will load your theme and open up the nautilus desktop.  In Lunchbox, every program has it's own workspace, which you can now try out by clicking the Program menu in the bottom Left Hand Side (LHS) of the screen. There should be an entry for XTerm and another entry for Nautilus.  Click on the entry for Nautilus.  The screen will change to show your normal desktop icons.

A workspace is meant to represent a different activity so it makes sense that it can a have a different arrangement of windows.

# Recovering Windows #

To place the xterm window in the nautilus workspace, use the Window menu (adjacent to the Program menu).  In general, only windows which are meant to be available in other workspaces (and make sense to be used in conjunction with other activities) are shown in this menu but at this stage only dialog boxes/transient windows are excluded from the list.

# Window Frame Controls #

A frame in the Lunchbox window manager can have the following controls:
  * 9 resize grips to resize in 9 different directions.
  * A close button
  * A Mode menu
  * A Title
  * A Title menu

# Mode Menu #

The tiny buttons typically used in other window managers are not sufficient to communicate the current state of the window or what modes are available. Therefore, the Lunchbox window manager offers the Mode Menu.
The Mode Menu shows the currently selected mode and allows the stacking mode to be changed to one of the following entries:

  * Floating. This is a traditional stacking mode. Dialog boxes/transient windows default to this do you don't have to rearrange everything to fit them in.
  * Tiling. A non-overlapping mode that most windows use by default.  If the window refuses to change to this mode, it means that there isn't enough room on the screen.  If two tiled windows are placed on the screen and placed next to each other they become "friends" and resizing one will cause the adjacent windows to be resized.  To disconnect the windows, move them away from each other.  Windows can specify a minimum and maximum size and Lunchbox will always respect this.
  * Desktop. This makes the window large enough to cover the whole screen except for the bottom menubar and places below all other windows (but on top of other desktop windows).
  * Hidden.  This hides the window and is like minimizing it.

To open the Mode menu, click on the current mode in the titlebar but make sure the pointer doesn't move before releasing the mouse button (a small bug).

# Title Menu #

The Title Menu is a scalable replacement to tabs. Tabs suffer from severe scalability problems and it can be hard to keep track of windows with ever-shrinking titles, especially when there are multiple sets of tabs. The Title Menu allows any window to be swapped with any other window, even windows which are hidden. To open the Title Menu, click on the title of the window in the titlebar but make sure the pointer doesn't move before releasing the mouse button (a small bug).

# Nifty Features #

  * Alt+Click and then dragging the mouse on a window. This can be used to grip and move windows by clicking anywhere on them. This is an idea borrowed from several other Linux Window Managers such as icewm and metacity.  It is particularly useful when a dialog box is larger than the screen and you need to move it further off the top of the screen to click the OK or Cancel buttons.

  * Clicking and dragging the mouse on the Title Menu or Mode Menu.  This still allows moving the window, allowing narrow windows without any empty space on their title bars to still be moved around the screen easily. As a side effect it leads to the two small bugs mentioned above.

  * Theming is straight-forward in Luchbox.  Look it up at http://code.google.com/p/lunchbox/wiki/Themes

  * The frame can be double clicked to maximize the frame.  If the frame is tiled, it is placed into the largest available space.  Frames must be resized manually to restore them to their previous size.