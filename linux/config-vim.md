# Config Vim

Config your vim

```bash
vim ~/.vimrc
```

For Python PEP8:

{% code-tabs %}
{% code-tabs-item title="~/.vimrc" %}
```text
" Filetype - Python
autocmd FileType python set shiftwidth=4 | set expandtab | set softtabstop=4 | set tabstop=4

filetype plugin on
```
{% endcode-tabs-item %}
{% endcode-tabs %}

For YAML:

{% code-tabs %}
{% code-tabs-item title="~/.vimrc" %}
```text
" Filetype - YAML
autocmd BufRead, BufNewFile *.yaml *.yml setfiletype yaml
autocmd FileType yaml set shiftwidth=2 | set expandtab | set softtabstop=2 | set tabstop=2

filetype plugin on
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Integration:

```text
" Filetype - Python
"" autocmd FileType python set shiftwidth=4 | set expandtab | set softtabstop=4 | set tabstop=4

" Filetype - YAML
autocmd BufRead, BufNewFile *.yaml *.yml setfiletype yaml
autocmd FileType yaml set shiftwidth=2 | set expandtab | set softtabstop=2 | set tabstop=2

filetype plugin on
```

