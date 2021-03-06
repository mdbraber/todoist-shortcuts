# todoist-shortcuts changelog

## Not yet released ##

* No longer attempts to reselect tasks after priority change as this
  triggers a bug. See
  [#32](https://github.com/mgsloan/todoist-shortcuts/issues/32).


## Version 15 ##

* Keyboard events not handled by todoist-shortcuts now get passed
  along to Todoist. See
  [#25](https://github.com/mgsloan/todoist-shortcuts/issues/25).

* Now supports navigation to favorite filters / labels. See
  [#31](https://github.com/mgsloan/todoist-shortcuts/issues/31).


## Version 14 ##

* Bump to Todoist version 908. This version of the extension fixes
  issues with todoist-shortcuts due to some recent changes of
  todoist's DOM structure.

* Improved reliability of task motion commands.

* Adds 'c' keybinding for opening comment dialog.


## Version 13 ##

* Enter can now be used to confirm deletion.

* Pressing escape will now exit out of inline task adding.

* Change "remove label" keybinding to use `@` instead of `l`.  The old
  keybinding shadowed the expand + navigate in keybinding.

* Cursor is now visible in filters and labels! See
  [#14](https://github.com/mgsloan/todoist-shortcuts/issues/14).

* Bump to Todoist version 907.


## Version 12 ##

* Removed some warnings which can occur during normal operation
  (particularly when no tasks are visible). Warnings that can happen
  during normal operation should only happen when the action can not be
  performed for some reason, and should be reasonably human readable.


## Version 11 ##

* Fixed icons


## Version 10 ##

* Due to Todoist making some changes to their code, it is now possible
  to use todoist-shortcuts with languages other than english.
  See [#2](https://github.com/mgsloan/todoist-shortcuts/issues/2)

* In navigate mode, `t` is no longer used to navigate to "Today",
  instead `g` is used. The main reason for this is that in navigate
  mode, it is now possible to use `tp` / `tl` / `tf` to toggle the
  different sections. These would not have b These would not have been
  typeable if `t` was taken. This also makes it a little faster to
  navigate to the commonly used "Today" section.

* Now supports navigating to labels and filters. See
  [#3](https://github.com/mgsloan/todoist-shortcuts/issues/3)

* In navigation mode, selecting a project with collapsed sub-projects will
  cause them to expand. To collapse, just re-select the same project.

* Adds `* l` and `* h` to expand or collapse all task nesting. See
  [#18](https://github.com/mgsloan/todoist-shortcuts/issues/18)

* `?` shortcut for keyboard shortcuts help now links to the readme for
  that particular release, rather than master.

* Typing "x" in an input field no longer toggles selection. See
  [#15](https://github.com/mgsloan/todoist-shortcuts/issues/15)

* There was a bug where after editing a task, the task before it would end
  up selected. This is now fixed. See
  [#9](https://github.com/mgsloan/todoist-shortcuts/issues/9)

* Some Todoist internals are now directly invoked, to handle
  selection more efficiently. See
  [#11](https://github.com/mgsloan/todoist-shortcuts/issues/11)

* Previously key sequences like `* a` required that you not delay more
  than 1 second between keystrokes, due to behavior in the
  [mousetrap](https://github.com/ccampbell/mousetrap) library. This
  is no longer the case.

* Fixes an issue where typing `g` followed by some key that does nothing
  would cause the cursor to move down one.

* Scrolling behavior and cursor mouse behavior is now less glitchy.

* `ctrl+z` is now a synonym for undo.

* Adds `* t` keybinding to enter bulk reschedule mode.

* Adds `* v` keybinding to enter bulk move mode.

* Using `h` to collapse will now collapse the parent if the cursor
  is already collapsed

* Using `l` to expand will now move the cursor to the first
  sub-project.

* `x` can no longer be held down to do multiple selections.  This is due
  to key sequences like `jxjxjxjx` being glitchy.  There is a constant
  called `MULTISELECT` in the source that can be set to `true` to bring
  back the multiselection behavior.

* Bump to todoist version 904.


## Version 9 ##

* Bump to todoist version 893.  Fixes for things that changed.

* Only has noisy version mismatch if your todoist version is too old.

* Now also works on https://beta.todoist.com/app

* Adding tasks via `o` and `O` now works when cursor is on an overdue task
  in agenda view

* Fixes to issues with cursor position after task add. See
  https://github.com/mgsloan/todoist-shortcuts/issues/8

* Old scheduling binding for "n" removed, use "d" instead.


## Version 8 ##

* Now uses the standard drag-and-drop handle to indicate the cursor.

* 'x' can be held down to select / deselect every task the cursor is moved to.

* Vertical auto-scrolling now takes into account top bar occlusion.


## Version 7 ##

* Bump to todoist version 892.

* No longer has a noisy warning by default for version mismatch.

* "r" for sort by assignee now works.

* Scheduling keybinding for "today" is now "d" instead of "n".

* Now "move to project" is back to being "v" instead of "m".


## Version 6 ##

* Bump to todoist version 891.

* Defaults to allow applying done / archive directly to cursor. Issue #1

* Implements sorting keybindings. Issue #1

* Adds "^" and "$" keybindings for moving cursor to first and last task.

* Cursor is now stable even when task gets re-scheduled or moved.

* When navigate mode is activated ("g"), the left pane will now become
  visible even when the browser window is narrow and so in 'mini mode'.


## Version 5 ##

* Bump to todoist version 890.

* Have mismatch warning tell you which version was expected.


## Version 4 ##

* Last version was hastily released, this fixes "move to project" (release
  made minutes after the last one)


## Version 3 ##

* Now "move to project" is "m" instead of "v".


## Version 2 ##

* Most default todoist keybindings like 'u' for undo now work too.

* Fixes position of version mismatch warning when viewing more
than a screenful.

* No longer warns about potential mismatch with todoist version 889
