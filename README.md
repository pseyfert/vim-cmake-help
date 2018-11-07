# vim-cmake-help
(yet another way of) getting cmake help inside vim with shift-k

Inspired by the [vim-go](https://github.com/fatih/vim-go) plugin, I figured I
could improve my cmake handling in vim. Searching before putting in some effort
on my side, I discovered also [vim-cmake](https://github.com/zchee/vim-cmake)
but appreciated the buffer handling by vim-go better (though both seemed a bit
complicated to me for not using `<cword>` and I didn't see an easy way to bodge
things together, so that's something I replaced on my side.

All the plugin does is open the result of `cmake --help-command <current word>`
upon the `shift-k` keystroke. And if that command fails, close the buffer
immediately. If there is already a Cmake documentation buffer, reuse it.

## deployment

The file sits atm in my `~/.vim/after/ftplugin/cmake.vim`.
