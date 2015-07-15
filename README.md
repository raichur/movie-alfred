# Record Movie with QuickTime Player

A simple [Alfred](http://alfredapp.com) workflow to open QuickTime Player and start recording a movie. Just type “movie” in Alfred.

In case you're wondering, here's the AppleScript behind it:

```
on alfred_script(q)
	tell application "QuickTime Player"
		set newMovieRecording to new movie recording
		set windowID to id of first window whose name = "Movie Recording"
		tell newMovieRecording
			start
		end tell
	end tell
end alfred_script
```

That's it!
