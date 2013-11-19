todo
====
Simple task management program

Version 0.0.1

This spec is not frozen at all.


Would like to write a simple yet scriptable TODO program.

Eventually want integration for notifications to devices, etc.

Usage
-----
If not passed any arguments, starts an interactive session. Otherwise:
-m --must <item>	Add a new item with high prority
-s --should <item>	Add a new item with medium prority
-w --want <item>	Add a new item with low prority
-f --finished <item>	Mark an item as done
-l --list		List the list

Addtional interactive-mode-only commands
-q --quit		Quit, saving changes
   --discard		Quit, discarding changes
   --swap <a> <b>	Swap two items
   --restore-previous   Swap current list with backup

Interactive session repeatedly accepts commands in the above form, without dashes.
 > Indicates user input and should not be entered
 < Indicates computer output and will not be printed

Example interactive todo session
--------------------------------
~$ todo
>must Fix seg fault bug in partition program
>w Better keyboard
>should Get car fixed
>list
<1) Fix seg fault bug in partition program
<2) Get car fixed
<3) Better keyboard
>q
~$

Potential features
------------------
Named lists
 * track sets of tasks independently
Simple backup
 * keeps a copy of list from prior to interactive session (so you can roll back changes)
Advanced backup
 * keeps complete revision history (via 'inverted' commands -- can undo every atomic step
