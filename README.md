# EditorConfig Vim Plugin

[![Build Status](https://travis-ci.org/editorconfig/editorconfig-vim.svg?branch=master)](https://travis-ci.org/editorconfig/editorconfig-vim)

This is an [EditorConfig][] plugin for Vim. This plugin could be found on both
[GitHub][] and [Vim online][].

## Installation

If your Vim is not compiled with `+python` feature (You can verify if the
`+python` feature is included by running `:ver`.  Most Linux distributions and
with the official Windows binary have the `+python` feature enabled), please
first download the [EditorConfig core][] and follow the instructions in the
README and INSTALL files to install it. This plugin would NOT work if neither
`+python` nor EditorConfig core is available.

To install this plugin, you can use either of the following ways:

- Download the archive and extract it into your Vim runtime directory (`~/.vim`
  on UNIX/Linux and `$VIM_INSTALLATION_FOLDER\vimfiles` on windows).

- Use [pathogen][] (the git repository of this plugin is
  https://github.com/editorconfig/editorconfig-vim.git)


## Supported properties

The EditorConfig Vim plugin supports the following EditorConfig [properties][]:

* `indent_style`
* `indent_size`
* `tab_width`
* `end_of_line`
* `charset`
* `insert_final_newline` ([PreserveNoEOL][] is required for this property)
* `trim_trailing_whitespace`
* `max_line_length`
* `root` (only used by EditorConfig core)

## Recommended Options

All of the options which are supported are documented in [editorConfig.txt][]
and can be viewed by executing the following: `:help editorconfig`.

#### Excluded patterns.

To ensure that this plugin works well with [Tim Pope's fugitive][], use the
following patterns array:

> let g:EditorConfig_exclude_patterns = ['fugitive://.\*']

If you wanted to avoid loading EditorConfig for any remote files over ssh:

> let g:EditorConfig_exclude_patterns = ['scp://.\*']

Of course these two items could be combined into the following:

> let g:EditorConfig_exclude_patterns = ['fugitive://.\*', 'scp://.\*']

#### Exec Path

The file path to the EditorConfig core executable. You could set this value in
your |vimrc| like this:

> let g:EditorConfig_exec_path = 'Path to your EditorConfig Core executable'

## Bugs and Feature Requests

Feel free to submit bugs, feature requests, and other issues to the
[issue tracker][].

[EditorConfig]: http://editorconfig.org
[EditorConfig core]: https://github.com/editorconfig/editorconfig-core
[GitHub]: https://github.com/editorconfig/editorconfig-vim
[issue tracker]: https://github.com/editorconfig/editorconfig-vim/issues
[pathogen]: https://github.com/tpope/vim-pathogen
[properties]: http://github.com/editorconfig/editorconfig/wiki/EditorConfig-Properties
[Vim online]: http://www.vim.org/scripts/script.php?script_id=3934
[PreserveNoEOL]: http://www.vim.org/scripts/script.php?script_id=4550
[Tim Pope's fugitive]: https://github.com/tpope/vim-fugitive
