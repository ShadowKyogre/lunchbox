Lunchbox is a new Window Manager for the X Windows System.  It aims to improve usability and allow more efficient use of screen space than traditional overlapping windows managers.

For example, if a window is moved off the edge of the screen it has reduced usability because scrollbars and other widgets such as close buttons are not visible.
In Lunchbox, moving a window against the edge of the screen squishes it, allowing the user to still access all of the windows contents using the scroll bar.

Overlapping windows typically present the same problem of hiding important widgets and reducing usability.  Therefore, the Lunchbox Window Manager offers a non-overlapping "tiling" mode by default.  Unlike other tiling window managers which have pre-determined layouts, tiled windows in Lunchbox can still be moved freely and resizing a tiled window causes adjacent windows to be resized.

In some cases stacking windows do make sense.  Dialog boxes for example. Therefore all windows can still be put into a "floating" mode using the Mode menu.

Another innovation is the introduction of the Title Menu.  The Title Menu is a scalable replacement to tabs.  Tabs suffer from severe scalability problems and it can be hard to keep track of windows with ever-shrinking titles, especially when there are multiple sets of tabs.
The Title Menu allows any window to be swapped with any other window, even windows which are hidden.

In Lunchbox, every program is meant to be about a different activity and present a different view.  So Lunchbox gives each program it's own unique arrangement of windows and individual workspaces.  This is useful in conjunction with tiled windows as it becomes simple to switch between a whole set of windows. It is good for separating "desktop" programs such as netbook-launcher and nautilus which no longer need to compete over the desktop - the user can simply choose the nautilus or netbook-launcher workspace from the Program menu.


It is compatible with most existing X11 Linux software and is working toward EWMH and ICCCM compliance.  It was created using the C programming language, Xlib, Xcursors and the Cairo graphics library.

Lunchbox was developed by Alysander Stanley as two advanced projects at Monash University  under the supervision of Dr David Squire.

Screenshots can be found in the Downloads section.