1.  Keep calm, your data are safe
2.  If the codeblocks are visible to the user, it means RPG Manager is not active
3.  Open the inspector window
4.  Open the Command Panel and run `Reload app without saving` and run the updater
5.  Check where the error is triggered. 90% of the times it is a malformed yaml in the codeblock
6.  The yaml that generates the error must be set in a single line (Obsidian sometimes create multilines) and surrounded by double quotes.
7.  If the text contains double quotes, they should be changed to single quotes
8.  once the file causing problems is fixed, open the Command Panel and run `Reload app without saving` and run the updater once more
9.  If other errors appear, go to 4