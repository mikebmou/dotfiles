fugitive.vim
============

I'm not going to lie to you; fugitive.vim may very well be the best
Git wrapper of all time.  Check out these features:

View any blob, tree, commit, or tag in the repository with `:Gedit` (and
`:Gsplit`, `:Gvsplit`, `:Gtabedit`, ...).  Edit a file in the index and
write to it to stage the changes.  Use `:Gdiff` to bring up the staged
version of the file side by side with the working tree version and use
Vim's diff handling capabilities to stage a subset of the file's
changes.

Bring up the output of `git status` with `:Gstatus`.  Press `-` to
`add`/`reset` a file's changes, or `p` to `add`/`reset` `--patch` that
mofo.  And guess what `:Gcommit` does!

`:Gblame` brings up an interactive vertical split with `git blame`
output.  Press enter on a line to reblame the file as it stood in that
commit, or `o` to open that commit in a split.  When you're done, use
`:Gedit` in the historic buffer to go back to the work tree version.

`:Gmove` does a `git mv` on a file and simultaneously renames the
buffer.  `:Gremove` does a `git rm` on a file and simultaneously deletes
the buffer.

Use `:Ggrep` to search the work tree (or any arbitrary commit) with
`git grep`, skipping over that which is not tracked in the repository.
`:Glog` loads all previous revisions of a file into the quickfix list so
you can iterate over them and watch the file evolve!

`:Gread` is a variant of `git checkout -- filename` that operates on the
buffer rather than the filename.  This means you can use `u` to undo it
and you never get any warnings about the file changing outside Vim.
`:Gwrite` writes to both the work tree and index versions of a file,
making it like `git add` when called from a work tree file and like
`git checkout` when called from the index or a blob in history.

Use `:Gbrowse` to open the current file on GitHub, with optional line
range (try it in visual mode!).  If your current repository isn't on
GitHub, `git instaweb` will be spun up instead.

Add `%{fugitive#statusline()}` to `'statusline'` to get an indicator
with the current branch in (surprise!) your statusline.

Oh, and of course there's `:Git` for running any arbitrary command.

Screencasts
-----------

* [A complement to command line git](http://vimcasts.org/e/31)
* [Working with the git index](http://vimcasts.org/e/32)
* [Resolving merge conflicts with vimdiff](http://vimcasts.org/e/33)
* [Browsing the git object database](http://vimcasts.org/e/34)
* [Exploring the history of a git repository](http://vimcasts.org/e/35)

FAQ
---

> I installed the plugin and started Vim.  Why don't any of the commands
> exist?

Fugitive cares about the current file, not the current working
directory.  Edit a file from the repository.

> I opened a new tab.  Why don't any of the commands exist?

Fugitive cares about the current file, not the current working
directory.  Edit a file from the repository.

> I changed the current working directory.  Why do all the commands use
> the old directory?

Fugitive cares about the current file, not the current working
directory.  Edit a file from the repository.

Self-Promotion
--------------

Like fugitive.vim? Follow the repository on
[GitHub](http://github.com/tpope/vim-fugitive) and vote for it on
[vim.org](http://www.vim.org/scripts/script.php?script_id=2975).  And if
you're feeling especially grateful, follow tpope on
[Twitter](http://twitter.com/tpope) and
[Github](http://github.com/tpope).
