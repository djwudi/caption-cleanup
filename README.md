# Caption Cleanup

Quick and dirty scripts to assist with caption and subtitle cleanup work after the subtitles or captions have been extracted and converted to .srt text files.

These are AppleScript scripts intended to work with BBEdit. I'm not very knowledagble in scripting or github, so don't expect much. I just tossed these together to do what I needed. If they help someone else? Bonus!

## Caption Cleanup

Used for cleaning Closed Caption sources that use standard capitalization.

In order:
* straightens quotes (from “curly quotes” to "straight quotes")
* removes multiple spaces used to force text placement location (so lines don't look `          like this  `)
* fixes spaces inside italic tags and parentheses (to correct for `<i> this </i>` or `( this )`)
* educates quotes (from "straight quotes" to “curly quotes”)
* fixes leading apostrophes for abbreviated words (from `‘cause` to `’cause`) and decades (from `‘50s` to `’50s`); **individual years will not be corrected** (such as `‘87` to `’87`) and will need to be done manually
* saves the file

## Caption Cleanup CAPS

Used for cleaning Closed Caption sources that use ALL CAPS.

In order:
* straightens quotes (from “curly quotes” to "straight quotes")
* changes the case of all text to capitalize sentences; because of the formatting of .srt files, **this will not properly capitalize all sentences**, and a manual final pass is necessary
* removes multiple spaces used to force text placement location (so lines don't look `          like this  `)
* fixes spaces inside italic tags and parentheses (to correct for `<i> this </i>` or `( this )`)
* corrects capitalization of most first-person singular "I" instances (such as "I", "I'd", "I'll", etc.); **this may not catch all instances**
* educates quotes (from "straight quotes" to “curly quotes”)
* fixes leading apostrophes for abbreviated words (from `‘cause` to `’cause`) and decades (from `‘50s` to `’50s`); **individual years will not be corrected** (such as `‘87` to `’87`) and will need to be done manually
* saves the file

## Abbrev Apostrophe Fix

Just the abbreviation leading apostrophe fix.

In order:
* educates quotes (from "straight quotes" to “curly quotes”)
* fixes leading apostrophes for abbreviated words (from `‘cause` to `’cause`) and decades (from `‘50s` to `’50s`); **individual years will not be corrected** (such as `‘87` to `’87`) and will need to be done manually

## Common OCR Fixes

Used for cleaning PGS or VobSub sources that have been OCR'd.

In order:
* replaces the `ﬂ` and `ﬁ` ligatures with `fl` and `fi`, respectively
* corrects the following errors:
  * `ofthe` to `of the`
  * `ofall` to `of all`
  * `Ijust` to `I just`
  * ` ?` and ` !` to `?` and `!`
