## Reason:

This command is for who has a big playlist holding thousands of tracks
like me. It `playnext` the song you select in playlist view, without
compromising your current playing queue, but you can still use the same
keybinding to play that track intermediately in the queue view.

Example:
Say you bind `Enter` to `playorplaynext` in your configuration file
When you press enter outside of queue view, the track you selected get
added to the queue, the same as you invoke `playnext`
But when you are in queue view, pressing enter just play the track you
selected, it is just more intuitive to me. And much more convenient: we
don't have to memorize two keys.

More to hack:
`ncspot`'s configuration file can't bind a single key to different
functions in different view. A good hack maybe fix the way that
`Command` works. A keystroke should invoke both a `Command` with its
`Context`, if current context is not the identical to the one passed in,
the command should be silently ignored, instead of always telling its
user you are making a big mistake.
