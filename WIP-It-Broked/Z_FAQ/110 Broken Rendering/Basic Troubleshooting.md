# Don't Panic, your data is safe! 
<img src="https://live.staticflickr.com/8360/8300870890_181382ff4a_b.jpg" width="500" height="375" alt="Don&#x27;t Panic" style="display: block; margin: auto">

## RPG Mananager Header Doesn't Render
This can occur at any time, usually due to malformated YAML in frontmatter keys that RPG Manager uses

1. On startup, or reload, RPG Manager will usually give you an error indicating notes with broken paths. Usually the malformated YAML is in the common ancestor of the failing notes.
    
    Ex: In the below example, the adventure "Adv 1" has malformated frontmatter, causing all its decendent notes to have pathing issues
    ![Pathing Issues](/Images/Pathing_Issue.png)

    The frontmatter (below) has the `synopsis` key split on multiple lines. Unless the key is itself a list (like `alias`), it needs to be surrounded by double quotes, and on a single line. If the text contains quotes, they need to be single quotes.
    ```
    ---
    alias: []
    tags:
    - rpgm/adventure/1/1
    completed: false
    synopsis: This is
        broken
    ---
    ```
1. If you correct the issues with the YAML and either restart or reload, the errors should resolve, and the RPG Manager headers should render. See blow for corrected exmpale

    ```
    ---
    alias: []
    tags:
    - rpgm/adventure/1/1
    completed: false
    synopsis: This is not broken
    ---
    ```
## Code Blocks Visible to User
This sometimes occurs during a version upgrade, usually due to malformated YAML

1. Open the inspector window (CTRL-SHIFT-I/Option-CMD-i)
1. Open the Command Panel and run `Reload app without saving` to re-run the updater
1. Check where the error is triggered via the inspector window. 90% of the times it is a malformed yaml in the codeblock
1. This should indicate which file has malformed YAML. Please correct it, observing the following requirements.
    1. YAML statements (that aren't lists) must be on a single line
    1. YAML values (not the keys) should be wrapped in double quotes
    1. Any quotes in the string should be converted to single quotes
1. Once the file causing problems is fixed, open the Command Panel and run `Reload app without saving` and run the updater once more


<p class="attribution">"<a target="_blank" rel="noopener noreferrer" href="https://www.flickr.com/photos/95142644@N00/8300870890">Don't Panic</a>" by <a target="_blank" rel="noopener noreferrer" href="https://www.flickr.com/photos/95142644@N00">Ruth and Dave</a> is licensed under <a target="_blank" rel="noopener noreferrer" href="https://creativecommons.org/licenses/by/2.0/?ref=openverse">CC BY 2.0 <img src="https://mirrors.creativecommons.org/presskit/icons/cc.svg" style="height: 1em; margin-right: 0.125em; display: inline;"></img><img src="https://mirrors.creativecommons.org/presskit/icons/by.svg" style="height: 1em; margin-right: 0.125em; display: inline;"></img></a>. </p>