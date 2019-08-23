# .gitattributes

```text

# Customizing Git - Git Attributes https://git-scm.com/book/en/v2/Customizing-Git-Git-Attributes
# gitattributes - Defining attributes per path https://git-scm.com/docs/gitattributes

# pattern	attr1 attr2 ...
# Each line in gitattributes file is of format

* text=auto
# Handle line endings automatically for files detected as text and leave all files detected as binary untouched
# Overwrites the local `core.autocrlf` settings, which ensures uniform behavior

*.css linguist-vendored
*.scss linguist-vendored
*.js linguist-vendored
# Uses the open source Linguist library to determine file languages for syntax highlighting and repository statistics
# Some files are hard to identify, and sometimes projects contain more library and vendor files than their primary code
# https://stackoverflow.com/a/34715182/3123272

CHANGELOG.md export-ignore
# You can tell Git not to export certain files or directories when generating an archive
# Now, when you run `git archive` to create a tarball of your project, that directory won’t be included in the archive
```
