# HOW TO USE THIS SASS ARCHITECTURE

## What to put in which directory

### HELPERS
Contains all variables, functions, and mixins, etc.

### BASE
Contains boilerplate stuff, including normalize, and basic stuff like
setting margins for <p> and <h1>, setting default font size and color,
things like that.

### LAYOUT
Contains styles for the general structure of the site.
Styles for things such as the header and footer go here - things that
appears on (almost) every page.

### COMPONENTS
Contains styles for components that may be used in various different
places. For example, buttons, search bars, carousels.

### PAGES
Contains page-specific styles, styles that are only required on ONE PAGE.
For example, your home page will probably need a lot of styles that aren't
reused anywhere else, that would go in pages/_home.scss.

## What to do when you add new files

In each folder, there is a single file with a corresponding name,
eg: pages/_pages.scss. This file should import every other file in that
folder. For subfolders, the same thing should happen,
eg: helpers/variables/_variables.scss.

main.scss should only ever contain imports. It should import the files in each
folder that import all the files in the folder (if that sounds complicated, 
just have a look at the code, it's v simple).