[dropshowcase.webm](https://github.com/sillybanaja/drop/assets/132526605/8e33ac5a-49c5-4fcf-a57f-e8bc4c1527b8)

---
I wanted a simple way to drag files from the terminal into windows that force
drag-and-drop without having to open a file browser or interact with a GUI.
Existing solutions like Dragon by mwh are "bloated" (written in GTK) for what I
need, plus required me to physically drag the files to the target application with
a gui which is not ideal.

I wrote drop in C using Xlib, which is lightweight and widely available on
Unix-like systems. It takes a list of filenames as arguments and allows you to
drop them onto any application that supports XDND, without requiring you to physically
drag the files.

To install or remove drop use the provided Makefile. Simply run a `make install` which
will install to /usr/local/bin (by default). To uninstall run `make uninstall`.

Usage: just type `drop filename ...` followed by the names of the files you want to drop.
You can also use globbing patterns like "**~/Downloads/*.jpg**". After pressing Enter,
you can navigate to the destination window and click where you want to drop the files.
Press Escape at any time to close the program.

Note that this implementation is a little crude, but it should work with most
applications that support drag-and-drop (XDND).

Pull requests and bug reports are welcome. Please keep in mind that this project
is intended to remain small and focused on its core functionality. 
