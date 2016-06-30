This is the program for the sixth RetroBattlestations BASIC
challenge. In here you'll find a simple BASIC program that uses a
stack based command interpreter to do "turtle graphics". The program
has been ported to several platforms already, but you're welcome to
add more!

Commands are put into a string called CM$ with values and commands
separated by a space. Numeric values will be pushed onto a stack, a
command will pop off a value and then execute. There is very little
error checking being done. There are four commands supported:

* D - lower the pen
* U - raise the pen
* M - move
* T - turn

Looping is done by putting a value on the stack representing the
number of iterations and then placing commands inside of ( ). There
must be a space separating the ( ) characters from the commands and
values inside.

I did my best to minimize "dirty tricks" although I did use some bit
fields for the Cohen-Sutherland line clipping algorithm. If you want
to know how the algorithm works, [see
here](http://www.tutorialspoint.com/computer_graphics/viewing_and_clipping.htm).

For more details about the challenge, check out the post here:

  http://RetroBattlestations.com

## Porting ##

If you are working on a port, choose the version to start with
carefully. Some BASIC interpreters support bitwise operators, some do
not. If you are working on a platform that *does* support bitwise
operators then you **do not** want to use the Apple II source as a
reference!

See [List of Computers With On-Board BASIC](https://en.wikipedia.org/wiki/List_of_Computers_With_On-Board_BASIC)

## Typing Tips ##

When typing the program in you can leave off any lines which begin
with REM, they are not needed for the program to run. On many
platforms you can leave out the whitespace between keywords and
operators. IBM BASIC is not one of those however.

*Note*: On the TRS-80 Color Computer and BBC Micro you need to include
      the spaces around any IF, AND, OR, or THEN statement.

If you make a mistake and don't want to retype the entire line, most
of the BASICs have a way to make corrections.

### Apple II computers ###

  On an Apple II+ use LIST <line number> to print the line with an
  error, then use ESC followed by A/B/C/D to move the cursor one step
  at a time. Position the cursor at the beginning of the line, then
  use the right arrow to move over the line and fix the error. Be sure
  to arrow all the way to the end of the entire line before you hit
  RETURN!

  On an enhanced Apple IIe, Apple IIc, or Apple IIgs you can also use
  ESC with the arrow keys. In 80 column mode (enter with PR#3) the
  cursor will change to a white block with a + in it, push ESC to drop
  out of movement mode.

### BBC Micro ###

  Use LIST <line number> to print the line with a mistake, then use
  the arrow keys to move up to the beginning of the line. Each press
  of the copy key will type in the character under the cursor. Make
  any necessary edits by just typing on the keyboard and using copy to
  avoid retyping everything.

### Commodore 64, Plus/4, and 128 ###

  Like the others, use LIST <line number> to display the line with
  problems, then use the arrow keys to move up and make any
  corrections. By pressing shift-INST you can insert a blank character
  if you missed something. Unlike the Apple II you don't need to arrow
  to the end of the line before pushing RETURN.

### TRS-80 model 100 ###

  This has to be the best built-in BASIC editor I've seen so far! Just
  type EDIT and the entire BASIC program will be loaded into the
  built-in word processor where you can make any changes you
  want. Press F8 to exit the editor and go back to BASIC.

### IBM Cassette BASIC, Disk BASIC, Advanced BASIC, GW-BASIC ###

  Type EDIT <line number> and it will print the line on the screen and
  put your cursor at the beginning of the line. Arrow left/right and
  you can use Insert & Delete to make corrections. Like Commodore
  BASIC, you don't need to arrow to the end of the line before pushing
  RETURN.

### TI-99/4A Extended BASIC ###

  Type the line number and then arrow up (FCTN+E) and it will enter
  edit mode with that line loaded.  You can move within the line with
  arrow left (FCTN+S) and arrow right (FCTN+D) and move to the
  previous or next line with arrow up (FCTN+E) or arrow down (FCTN+X).
  You can delete the character under the cursor with DEL (FCTN+1) or
  turn on insert mode to insert extra characters with INS (FCTN+2).
  You do not need to move to the end of the line before pressing
  ENTER.
