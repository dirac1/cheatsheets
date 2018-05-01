bash/zsh keyboard shortcuts
======================

Move cursor
----------
* Ctrl + a 	Go to the beginning of the line (Home)
* Ctrl + e 	Go to the End of the line (End)
* Alt  + b 	Back (left) one word
* Alt  + f 	Forward (right) one word
* Ctrl + f 	Forward one character
* Ctrl + b 	Backward one character
* Ctrl + xx 	Toggle between the start of line and current cursor position

Edit
----------
* Ctrl + u 	Cut the line before the cursor position
* Alt  + Del 	Delete the Word before the cursor
* Alt  + d 	Delete the Word after the cursor
* Ctrl + d 	Delete character under the cursor
* Ctrl + h 	Delete character before the cursor (backspace)
* Ctrl + w 	Cut the Word before the cursor to the clipboard
* Ctrl + k 	Cut the Line after the cursor to the clipboard
* Alt  + t 	Swap current word with previous
* Ctrl + t 	Swap the last two characters before the cursor (typo)
* Esc  + t 	Swap the last two words before the cursor.
* Ctrl + y 	Paste the last thing to be cut (yank)
* Alt  + u 	UPPER capitalize every character from the cursor to the end of the current word.
* Alt  + l 	Lower the case of every character from the cursor to the end of the current word.
* Alt  + c 	Capitalize the character under the cursor and move to the end of the word.
* Alt  + r 	Cancel the changes and put back the line as it was in the history (revert)
* Сtrl + _ 	Undo

History
--------
* Ctrl + r 	Recall the last command including the specified character(s)(equivalent to : vim ~/.bash_history).
* Ctrl + p 	Previous command in history (i.e. walk back through the command history)
* Ctrl + n 	Next command in history (i.e. walk forward through the command history)
* Ctrl + s 	Go back to the next most recent command.
* Ctrl + o 	Execute the command found via Ctrl+r or Ctrl+s
* Ctrl + g 	Escape from history searching mode
* Alt  + . 	Use the last word of the previous command

Miscellaneous
-------------
* Ctrl + y	Paste from Kill Ring
* Ctrl + l	Clear screen
* Ctrl + o	Execute command but keep line
* Ctrl + z	Suspend process
* Ctrl + c	Kill current process
* Ctrl + d	Exit shell

Bang(!)
-------
* !!    	run last command
* !blah 	run the most recent command that starts with ‘blah’ (e.g. !ls)
* !blah:p 	print out the command that !blah would run (also adds it as the latest command in the command history)
* !$		the last word of the previous command (same as Alt + .)
* !$:p 		print out the word that !$ would substitute
* !* 		the previous command except for the last word (e.g. if you type ‘find some_file.txt /‘, then !* would give you ‘find some_file.txt‘)
* !*:p 		print out what !* would substitute
