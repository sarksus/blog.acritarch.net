+++
title = "Zola Post Snippet" 
date = 2024-10-13T00:35:07-04:00
authors = ["sarksus"]
[taxonomies]
tags = ["Site"]
+++

In addition to the iOS shortcut to post from my phone, I also set up a VS Code snippet that generates the Zola frontmatter each post needs when I want to post from my desktop computer. The snippet is as follows:


```json
"zolaPost": {
    "prefix": "zolaPost",   // the prefix is what you type in and hit tab in order to trigger the snippet to generate the frontmatter
    "scope": "markdown",    // what file type should this snippet be enabled for
    "body": [               // the contents of the snippet
        "+++",
        "title = \"${TM_FILENAME/[0-9]+-[0-9]+-[0-9]+[ ](.*).md$/$1/}\" ",  // this monstrosity takes in the filename using a built-in variable TM_FILENAME and then captures the title out of it
        "date = ${CURRENT_YEAR}-${CURRENT_MONTH}-${CURRENT_DATE}T${CURRENT_HOUR}:${CURRENT_MINUTE}:${CURRENT_SECOND}${CURRENT_TIMEZONE_OFFSET}",    // generates an ISO datetime
        "authors = [\"sarksus\"]",
        "[taxonomies]",
        "tags = [$2]",  // this is a tabstop, when the snippet is generated I can hit tab to move around these locations and type in whatever I want
        "+++"
    ],
    "description": "zolaPost"
}
```

Note that tab-completions have to be enabled in VS Code to work with this.

This is the frontmatter that was generated from the `2024-10-13 Zola Post Snippet.md` file:

```text
+++
title = "Zola Post Snippet" 
date = 2024-10-13T00:35:07-04:00
authors = ["sarksus"]
[taxonomies]
tags = ["Site"]
+++
```

So I create a new post file, type `zolaPost` and hit tab and it generates the frontmatter, I fill in the tags and then tab out to the end and write my post!

Note to self, I need to update the code block theming so it matches my site theme better. This is the first time using it and the default theme doesn't match very well.