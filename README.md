# jottem

jottem is a tool used to keep track of terminal sessions by creating temporary notes corresponding to a terminal specific session for those who either have a lot of thoughts running through their mind at any given time or just a lot of terminals/tmux sessions open

### installation

Simply put the `jot` script on your path (such as moving to `/usr/bin`) and run 

`$ jot` 

anytime to jot down some notes about your current work. It will prompt you accordingly 

### how it works 

If this is a terminal session that has never had any notes taken for it (the numerical result of running the command `tty`) then new notes will be created in `/tmp` with the name `jottem_<session number>.txt`.

If this is either an existing session or a session with a repeat number (which is bound to happen) jottem will give you three options:

1. edit the current notes (just append to what already exists)
2. archive the notes by moving them to `~./jottem_archive` and renaming the notes to have the date appended to the filename
3. delete the notes and start fresh like crisp autumn air 


### usage 

Either simply run 

`$ jot`

or, if you'd like to view notes for an existing session run 

`$ jot --view`

### TODO 

account for more possibilities such as:
* you create multiple terminal sessions in one day and want to archive multiple notes (right now it overwrites the archived notes)
* add help message 
* ?
