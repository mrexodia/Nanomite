#Nanomite - Windows Debugger for x64 and x86

## Features
- Debugging x86 and x64 (+ WOW64) processes
- Breakpoints
    - Software
		- Sizes: 1,2 and 4 bytes
		- Types: INT3, UD2, HLT
		- OnExecution
	- Memory
		- OnExecution, OnAccess and OnWrite
	- Hardware
		- Sizes: 1,2 and 4 bytes
		- OnExecution, OnRead and OnWrite
- Step In
- Step Over
- Step Out
- Step back to user code
- Attaching
- Detaching
- Single Step Tracing
- Supporting child processes
- Supporting multithreading
- Display source code
- Patching of instructions
- Bookmarks
- Comments
- Save and load project files
- Detailed view of:
	- disassembly
	- windows
	- handles
	- debug strings
	- threads
	- (child)processes
	- exceptions
	- process privileges
	- loaded modules
	- strings
	- callstack
	- stack
	- heap
	- cpu registers
	- functions
	- pe header
	- TEB/TBI
	- PEB/PBI

### Hotkeys
- most windows can be closed with "esc"
- most windows can be reloaded with "F5"
- STRG + C can be used to copy data from selected field in table - for more check context menu
- MainWindow
	+ STRG + B		= Breakpoint Manager
	+ STRG + O		= Open new file
	+ STRG + R		= Restart debugging
	+ STRG + I		= Show detail info window
	+ STRG + T		= Show trace window
	+ STRG + P		= Show patch window
	+ STRG + A		= Show attach window
	+ STRG + S		= Stop debugging
	+ STRG + D		= Detach from debuggee
	+ ALT + 1		= Show memory window
	+ ALT + 2		= Show heap window
	+ ALT + 3		= Show string window
	+ ALT + 4		= Show debug output window
	+ ALT + 5		= Show handle window
	+ ALT + 6		= Show windows window
	+ ALT + 7		= Show peeditor window
	+ ALT + 8		= Show function window
	+ ALT + 9		= Show process privilege window
	+ ALT			= Select menu bar and navigate with arrows
	+ F6			= Step Out
	+ F7			= Step In
	+ F8			= Step Over
	+ F9			= Start/Continue debugging
	+ F12			= Options
	+ Break			= Suspend debugging
- Attach Dialog
	+ Return		= Attach to selected process
	+ Double Click	= Attach to selected process
- Breakpoint Manager
	+ Del			= Remove selected breakpoint
	+ Double Click	= Send offset to disassembler
- Disassembler Window
	+ F2			= Set software breakpoint to selected line
	+ F4			= Execute until selected line
	+ Return		= Follow selected jump, call
	+ Backspace		= Go back after goto/follow
	+ Space			= Edit selected Instruction
- Function Window
	+ Double Click	= Show selected function in diassembler
	+ Return		= Show selected function in diassembler
- Options
	+ Del			= Remove selected custom exception
- Patch Manager
	+ Del			= Remove selected patch
	+ Return		= Send selected offset to disassembler
	+ Double Click	= Send selected offset to disassembler
- Register Window
	+ Double Click	= Opens reg edit window
- Trace Window
	+ Double Click	= Send selected offset to disassembler

## Changelog
###Version 0.1 beta 17
+ fixed a bug in the internal exception handler which could cause a termination on windows 8.1
+ fixed a bug which made patching jumps impossible
+ added option for "DebugSetProcessKillOnExit"
+ added option to load symbols from ms servers
+ added execute to selected line
+ added possibility to toggle eflags directly from context menu in the register view
+ improved internal PE file handling
+ improved copy to clipboard context menu

####Notes:
	- You can now copy multi lines to the clipboard using the context menu

###For the full changelog click [here](https://github.com/zer0fl4g/Nanomite/blob/master/changelog.md)