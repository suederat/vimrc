# vimrc
Clean up old vim config
 
$ cd    # go to $HOME
$ tar czf vim-config-bak.tgz .vimrc .vim/
 
Delete old config
$ rm -rf .vimrc .vim/
 
Start a fresh
$ mkdir -p .vim/bundle/
 
Clone Vundle (which is a VIM plugin that makes it easier to install VIM Plugins)
Link: https://github.com/VundleVim/Vundle.vim#quick-start
 
$ git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
 
Save the attached vimrc to your home-dir, then rename it.
 
$ mv vimrc .vimrc
 
Start Vim, download plugins, and restart vim
 
#Either
========
$ vim +PluginInstall +qall
 
#Or,
 
$ vim
 
#in vim
:PluginInstall
========
 
#Then, in vim
:qa! #or type 'ZQ'
 
Start vim, review .vimrc (I did my best to document my vimrc, including all the plugins, so it should be easy to delete what you don't like): 
 
$ vim ~/.vimrc
 
Get a visual cheatsheet. Take your pick...
https://www.google.com/search?q=vim+cheat+sheet&tbm=isch
 
I prefer these: 
 
(QWERTY) http://www.viemu.com/vi-vim-cheat-sheet.gif
(Dvorak, I'm weird) http://www.viemu.com/vi-vim-dvorak-cheat-sheet.gif
 
=======
My VIMRC
 
The most contentious part about my VIMRC will be the mappings. I'm not going to go into detail about all of these, but I should highlight them because they make my workflow a lot easier.
 
I've changed the 'map leader' to ',' (from '\') Everybody that uses the map leader changes it because '\' is hard to reach, however using ',' removes the ability to 'reverse search find char' see: t/T/f/F in the mappings. Some people end up using the spacebar instead, but I use spacebar for auto folding 'za'.
 
Here's my condensed mappings
,ve   - Edit VIMRC
,vs   - Source VIMRC
,/    - Clear '/' search highlighting
,n    - Toggle line numbers
,r    - Toggle relative line numbers
,l    - Toggle 'list' characters (visually represent whitespace characters like tabs and returns)
,bp   - Buffers, previous (':help buffers')
,bn   - ", next
,bN   - ", new
,bl   - ", list
,be   - ", Buffer Explorer plugin (very useful)
,tp   - Tabs, previous ('help tabs')
,tn   - ", next
,tN   - ", new
,tl   - ", list
,wn   - Windows, new horizontal window   (':help CTRL-W')
,wN   - ", new vertical window
,wp   - ", previous
,wq   - ", close (buffer still exists)
,ws   - ", split (buffer exists in both windows)
,wv   - ", vertical split (")
,ww   - ", next window
,wW   - ", previous window
,wT   - ", move to the far right
,N    - Toggle NERDTreeExplorer (Pretty file explorer in left pane)
,a    - Toggle Airline (Pretty statusbar, tabbar)
,pk   - Pymode, search python documentation
,pr   - ", run script
,pb   - ", set breakpoint
,pc   - ", Toggle Linting (Pylint, pyflakes, pylama)
,c    - Syntastic plugin (Generic Syntax checker for most languages)
,u    - UndoTree plugin (helps navigate vim's undo tree which is nearly impossible w/o a plugin)
,s    - Toggle Syntax highlighting
 
