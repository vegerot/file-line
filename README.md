# File-line

`file-line` is a plugin for Vim that enables opening a file in a given line.

This is a personal fork of
[github.com/bogado/file-line](https://github.com/bogado/file-line).  The fork
was created to address [this](https://github.com/bogado/file-line/issues/52)
issue, but since the code was so short I decided to rather rewrite it and do
some simplifications.

## Installation

If you use [vim-plug](https://github.com/junegunn/vim-plug), then add the
following line to your `vimrc` file:

```vim
Plug 'lervag/file-line'
```

Or use some other plugin manager:
- [vundle](https://github.com/gmarik/vundle)
- [neobundle](https://github.com/Shougo/neobundle.vim)
- [pathogen](https://github.com/tpope/vim-pathogen)

## Usage

When you open a `file:line`, for instance when coping and pasting from an error
from your compiler vim tries to open a file with a colon in its name.

Examples:

    vim index.html:20
    vim app/models/user.rb:1337

With this little script in your plugins folder if the stuff after the colon is
a number and a file exists with the name specified before the colon vim will
open this file and take you to the line you wished in the first place.

## Configuration

```vim
" Specify fallback if column is not specified
" * True: Go to first column in line (like normal |)
" * False: Go to first nonblank column (like normal ^)
let g:file_line_fallback_column0 = 1

" Disable flashing crosshairs on the cursor line/column
let g:file_line_crosshairs = 1

" Customize crosshairs behaviour
let g:file_line_crosshairs_number = 2
let g:file_line_crosshairs_duration = 200
```

## License

This script is licensed with GPLv3.

