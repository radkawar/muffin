Muffin is a fork of Mutter, specifically adapted to work as the window manager for the Cinnamon desktop environment.

The Debian packages enable the existing PipeWire screen cast and remote desktop
backends (`remote_desktop=true`). Applications still obtain user consent through
the desktop portal; this build option supplies the compositor interfaces used by
that backend, not a persistent portal permission.

The X11 virtual keyboard accepts evdev keycodes, matching the native backend.
Smooth scroll deltas accumulate into X11 wheel events instead of being ignored.
These are the existing Mutter fixes from merge requests !1732 and !1727.

# Mutter

Mutter is a Wayland display server and X11 window manager and compositor library.

When used as a Wayland display server, it runs on top of KMS and libinput. It
implements the compositor side of the Wayland core protocol as well as various
protocol extensions. It also has functionality related to running X11
applications using Xwayland.

When used on top of Xorg it acts as a X11 window manager and compositing manager.

It contains functionality related to, among other things, window management,
window compositing, focus tracking, workspace management, keybindings and
monitor configuration.

Internally it uses a fork of Cogl, a hardware acceleration abstraction library
used to simplify usage of OpenGL pipelines, as well as a fork af Clutter, a
scene graph and user interface toolkit.

Mutter is used by, for example, GNOME Shell, the GNOME core user interface, and
by  Gala, elementary OS's window manager. It can also be run standalone, using
the  command "mutter", but just running plain mutter is only intended for
debugging purposes.

## Contributing

To contribute, open merge requests at https://gitlab.gnome.org/GNOME/mutter.

The coding style used is primarily the GNU flavor of the [GNOME coding
style](https://developer.gnome.org/programming-guidelines/stable/c-coding-style.html.en)
with some minor additions such as preferring `stdint.h` types over GLib
fundamental types, and a soft 80 character line limit. However, in general,
look at the file you're editing for inspiration.

Commit messages should follow the [GNOME commit message
guidelines](https://wiki.gnome.org/Git/CommitMessages). We require an URL
to either an issue or a merge request in each commit.

## License

Mutter is distributed under the terms of the GNU General Public License,
version 2 or later. See the [COPYING][license] file for detalis.

[bug-tracker]: https://gitlab.gnome.org/GNOME/mutter/issues
[license]: COPYING
