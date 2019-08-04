# vim-floaterm

This plugin help toggle (floating) terminal quickly, detached from my [dotfiles](https://github.com/voldikss/dotfiles)

## Installation

```vim
Plug 'voldikss/vim-floaterm'
```

## Variables

#### **`g:floaterm_type`**

- Available: `'floating'`, `'normal'`

- Default: `'floating'`

#### **`g:floaterm_width`**

- Type: number

- Default: value of `&columns`

#### **`g:floaterm_height`**

- Type: number

- Default: value of `winheight(0)/2`

## Command

```
:ToggleTerminal
```

## Configuration

Recommended configuration

```vim
noremap  <silent> <expr><F12>     &buftype =='terminal' ?
                                  \ "\<C-\><C-n>:call util#toggleWindows('terminal')\<CR>" :
                                  \ "\<Esc>:call util#toggleWindows('terminal')\<CR>i<C-u>"
noremap! <silent> <F12>           <Esc>:call util#toggleWindows('terminal')<CR>i
tnoremap <silent> <F12>           <C-\><C-n>:call util#toggleWindows('terminal')<CR>
```

## Todo

- [ ] add doc
