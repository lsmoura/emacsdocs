Emacs CheatSheet
================

General
-------

	C-g	Cancel current command
	ESC ESC ESC    Cancel current command

	C-u <NUMBER> <COMMAND>	      Pass 'number' parameter to 'command'.
	    	Usually this is used for repetition, but can mean special uses on
		specific commands

	C-h c <COMMAND>	 Displays the brief description of 'command' on the minibuffer.
	C-h k <COMMAND>	 Open help on a separate window.
	        Change to that window (C-x o) and press 'q' to close the window or
		revert to previous buffer.
		If you want to work with only one window, you can just close all
		other windows with C-x 1
	C-h f <FUNCTION> Same as C-h k, but for a function name.
	C-h a <TEXT> Search help for all command with 'text'.
	C-h i 	Read the included manuals.
	
	C-/	Undo. Only works with buffer changes. Cursor movement is not "undoed".
		Text removed with undo cannot be yanked.
	C-_	Undo
	C-x u	Undo

	C-x C-c	Exit emacs

Movement
--------

	C-v	Next page
	M-v	Previous page

	C-f	Move forward a character
	C-b	Move backward a character

	M-f	Move forward a word
	M-b	Move backward a word

	C-n	Move to next line
	C-p	Move to previous line

	C-a	Move to beginning of line
	C-e	Move to end of line

	M-a	Move back to beginning of sentence
	M-e	Move forward to end of sentence

	M-<	Move to the begginning of the current buffer
	M->	Move to the end of the current buffer

	M-}	Move forward a paragraph
	M-{	Move backward a paragraph

	C-M-v	Next page on the next buffer (useful to look trough documentation without changing windows)

	C-l	Move the current buffer line to the middle of the window. On the second time (C-l C-l),
		the line is moved to the top of the window.
		Note that this does not changes the buffer contents, only its position on the screen.

Screen
------

	C-x o	Make next window active
	C-x 0	Close current window
	C-x 1	One window. Close all other windows
	C-x 2	Split current window horizontally (new window will appear on the bottom)
	C-x 3	Split current window vertically (new window will appear on the right)

Buffer
------

	C-x b	Change current buffer (input new buffer name on the minibuffer)
	C-x C-b	Open list of buffers on a new window
	C-4 4 b	Change the current buffer to the next window (or opens a new window for the buffer).
	      	The active window will be changed to the newly opened one.

Text Manipulation
-----------------

	<DEL>	Delete character just before the cursor (does not save for yanking)
	C-d	Delete the next character after the cursor (does not save for yanking)

	M-<DEL>	Kill the word immediately before the cursor (can be yanked)
	M-d	Kill the next word after the cursor (can be yanked)

	C-k	Kill from the cursor until the end of the line (can be yanked). Does not remove the linebreak.
		When used with C-u, it removes the whole line, including the linebreak. The whole repetition
		will be yanked at once.
	M-k	Kill until the end of the current sentence (can be yanked)

	C-<SPC>	Mark set on the current cursos point ("Mark set" message will be displayed on minibuffer)
	C-w	Kills the text from the Marked set until current cursor point (can be yanked)
	M-w	Saves the currently selected text to the yank buffer.
	C-x C-x	Exchanges the position of the cursor and the mark.

	M-h 	Marks the current paragraph.
	C-x C-p	Marks the current page.
	C-x h	Marks the current buffer.

	C-y	Yank the text
	M-y	Immediately after the text was yanked it changes to the previous buffer
		until it "wraps around".
	
### Searching

Remember that C-g can also be used to cancel your search.

If you type a control or meta character in the middle of your search, the search will be terminated.


	C-s	Start forward search.
		The search is performed live as the user types. Once the search term is to the user liking,
		repetitive C-s will move to the next match.
		When moving forward with C-s, <DEL> will move you back in search until the first found term.
		Type <Return> to terminate the search.
	C-r	Start reverse (backward) search


Files
-----

	C-x C-f	Find (open) file
	C-x C-s Save current buffer. If the buffer is already linked to a file, the file is saved.
	    	If the current buffer is not yet linked to a file, a filename will be requested
		at the minibuffer.
	C-x C-w	Saves the current buffer to a file. This prompts for a filename on the minibuffer.
	C-x s	Save all unsaved buffers. The user will be asked to confirm the save for each buffer.
	C-x 4 C-f
	C-x 4 f	Find (open) file on another window. Moves the cursor to the newly open buffer.

	C-x i 	Appends a file to the cursor location on the current buffer.

Commands
--------

	C-x	Character extend. A command with one character (like C-s, for saving or 1 for closing other
		windows.
	M-x	Named command extend. Type in the name of the command you wish to execute.
		eg. M-x save-buffer


Useful extended commands
========================

Extended commands are strings entered after M-x. They are single strings. You can use <SPC> to autocomplete
the commands.

Most of the commands support undo (C-/). The undo will revert all changes a command did, not just the last one.

     	version	     	Displays the current emacs version on minibuffer
	replace-string	Replaces all occurrences of one string with another. Takes two parameters,
			press <Return> after each parameter. You can undo this command; it will
			revert all of the changes the command did.

	revert-buffer	Reverts all the changes made to the current buffer
			since it was crated or last saved.

	text-mode
	fundamental-mode

Frames
------

	make-frame	Create another frame on the screen. On text terminals only one frame can be
			shown at a time.
	delete-frame	Removes the selected frame. This cannot be used to close the last open frame.

