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
<pre>
-m --must <item>         Add a new item with high prority
-s --should <item>       Add a new item with medium prority
-w --want <item>         Add a new item with low prority
-f --finished <item>     Mark an item as done
-l --list          List the list
</pre>

Addtional interactive-mode-only commands
<pre>
   --swap                Swap two items (still working on format)
-q --quit                Quit, saving changes
   --discard             Quit, discarding changes
   --restore-previous    Swap current list with backup
</pre>

Interactive session repeatedly accepts commands in the above form, without dashes.
<pre>
 &gt; Indicates user input and should not be entered
 &lt; Indicates computer output and will not be printed
</pre>

Example interactive todo session
--------------------------------
<pre>
~$ todo
&gt;must Fix seg fault bug in partition program
&gt;w Better keyboard
&gt;should Get car fixed
&gt;list
&lt;1) Fix seg fault bug in partition program
&lt;2) Get car fixed
&lt;3) Better keyboard
&lt;q
~$
</pre>
Potential features
------------------
Named lists
 * track sets of tasks independently
Simple backup
 * keeps a copy of list from prior to interactive session (so you can roll back changes)
Advanced backup
 * keeps complete revision history (via 'inverted' commands -- can undo every atomic step
