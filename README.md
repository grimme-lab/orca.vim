# Vim syntax for Orca

This project provides syntax highlighting for the [Orca quantum chemistry](https://orcaforum.kofo.mpg.de/app.php/portal) program compatible with the Orca 5.0.2 release.


## Syntax highlighting

Add the file in `syntax/orca.vim` to your *vim* runtime directory (*e.g.* `~/.vim/syntax/orca.vim`).


## File type detection
### Vim
Add these lines to your *vim* runtime directory in `ftdetect/orca.vim` to use the Orca syntax highlighting for all files ending in `.orca` and files named `orca.inp`.

```vim
" For vim >= 8
au BufRead,BufNewFile *.orca set filetype=orca
au BufRead,BufNewFile orca.inp set filetype=orca
```
### Neovim
Add these lines to your *lua* configuration files to use the Orca syntax highlighting for all files ending in `.orca` and files named `orca.inp`.
```lua
-- For neovim >= 0.8
local create_autocmd = vim.api.nvim_create_autocmd
local events = {"BufRead", "BufNewFile"}
create_autocmd(events, { pattern = {"*.orca"}, command = [[ set filetype=orca ]]})
create_autocmd(events, { pattern = {"orca.inp"}, command = [[ set filetype=orca ]]})
```


## Similar projects

- [mrymtsk/orca-vim](https://github.com/mrymtsk/orca-vim) by Toshiki Murayama ([@mrymtsk](https://github.com/mrymtsk))


## License

Licensed under the Apache License, Version 2.0 (the “License”);
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an *“as is” basis*,
*without warranties or conditions of any kind*, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in this project by you, as defined in the
Apache-2.0 license, shall be licensed as above, without any additional
terms or conditions.
