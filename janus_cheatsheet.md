# Vim (Janus plugins) Cheatsheet
    <Leader> is mapped to ','
    C is Ctrl

## Tree Operations
    <Leader>-n - Toggle tree pane
    <Leader>-nf - Find current buffer in the tree
    m - Display tree modification options (add, move, delete, copy) [Displayed when cursor is in tree]

## Window Navigation
    C-w-direction -  Move to the window in the desired direction (up, down, left, right)

## Window splitting
    :sp - Split the current buffer horizontally
    :vs - Split the current buffer vertically

## Buffer exploration
    <Leader>be - List currently open buffers
      <CR> - opens the buffer for editing
    <Leader>bs - Create a horizonal split window, leaving the current buffer visible and showing other open buffers in the split
    <Leader>bv - Create a vertical split window, leaving the current buffer visible and showing other open buffers in the split

## Cucumber
    C-] - Jump to step from feature

## String toggleing (Specky plugin)
    C-s' - Toggles between single quote, double quote (and symbol in Ruby)

## Ruby
    <Leader>bl - Toggle a block boundary between {} and do/end

## RSpec (Specky plugin)
    :A - Change view to alternate file (moves to related spec for a given file, or to file from related spec)
    C-ss - Run current RSpec buffer and display result
      q - Close window from RSpec test result

## Git (Fugitive plugin)
    :Gstatus - Display the git status for the current workspace
      <C-N> next file
      <C-P> previous file
      <CR>  |:Gedit|
      -     |:Git| add
      -     |:Git| reset (staged files)
      C     |:Gcommit|
      cA    |Gcommit| --amend --reuse-message=HEAD
      ca    |Gcommit| --amend
      D     |:Gdiff|
      ds    |:Gsdiff|
      dp    |:Git!| diff (p for patch; use :Gw to apply)
      dp    |:Git| add --intent-to-add (untracked files)
      dv    |:Gvdiff|
      O     |:Gtabedit|
      o     |:Gsplit|
      p     |:Git| add --patch
      p     |:Git| reset --patch (staged files)
      q     close status
      R     reload status
    :Gblame - Show git blame for the current buffer
      q     close blame and return to blamed window
      gq    q, then |:Gedit| to return to work tree version
      i     q, then open commit
      o     open commit in horizontal split
      O     open commit in new tab
      <CR>  reblame at commit
      ~     reblame at [count]th first grandparent
      P     reblame at [count]th parent (like HEAD^[count])

## Bundler
    :Bopen[!] [gem] - With no argument, edits the Gemfile.  Otherwise, effectively does a `bundle open` of a gem inside of Vim, including an |:lcd| to the gem's root directory.
    :Bsplit[!] [gem] - Like |:Bopen|, but horizontally split.
    :Bvsplit[!] [gem] - Like |:Bopen|, but vertically split.
    :Btabedit[!] [gem] - Like |:Bopen|, but use a new tab.

## CTags
    <F8> - Toggle open/close tag list window for the current buffer
