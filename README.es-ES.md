

# lf-vim

Resaltado de sintaxis de Vim para el archivo de configuración [lf](https://github.com/gokcehan/lf) (`lfrc`).

## Ahora parte de Vim y Neovim

**Este plugin se ha integrado en Vim (9.1.0778 y superiores) y Neovim (0.11 y superiores), por lo que debería funcionar directamente con las versiones recientes de estos programas.**

Este repositorio de GitHub rastrea la última versión en desarrollo del plugin. Puedes crear incidencias y pull requests aquí, para que los cambios sean enviados posteriormente al repositorio de Vim.

## Instalación

- Vundle:

    ```vim
    Plugin 'andis-sprinkis/lf-vim'
    ```

- vim-plug:

    ```vim
    Plug 'andis-sprinkis/lf-vim'
    ```

- lazy.nvim:

    ```lua
    { 'andis-sprinkis/lf-vim', event = { 'BufReadPre lfrc' } }
    ```

- Sin gestor de plugins:

    Copia todos los directorios de este repositorio en tu directorio `~/.vim/` (o en `${XDG_DATA_HOME:-~/.local/share}/nvim/plugged` para usuarios de Neovim).

## Sintaxis de Shell

Para resaltar los comandos de shell, este plugin utiliza el patrón `syntax include` de Vimscript `syntax/sh.vim` (el preset `sh`, `ksh`, `bash` incluido en Vim).

Se puede cambiar utilizando las variables:

| Configuración                | Variable            |
| ---------------------------- | ------------------- |
| La configuración global      | `g:lf_shell_syntax` |
| Una configuración local al búfer | `b:lf_shell_syntax` |

Por ejemplo:

```vim
" Vimscript (Vim, Neovim), init.vim
let g:lf_shell_syntax = "syntax/dosbatch.vim"
let b:lf_shell_syntax = "syntax/zsh.vim"
```

```lua
-- Lua (Neovim), init.lua
vim.g.lf_shell_syntax = "syntax/dosbatch.vim"
vim.b.lf_shell_syntax = "syntax/zsh.vim"
```

---

Consulta el directorio `$VIMRUNTIME/syntax` para ver las opciones de sintaxis disponibles (`:echo $VIMRUNTIME`).

## Capturas de pantalla

![screenshotLf](https://i.imgur.com/jdQU7nB.png)

![screenshotShell](https://i.imgur.com/ReZoGj9.png)

Esquema de colores utilizado para estas capturas de pantalla: [badwolf](https://github.com/sjl/badwolf "badwolf on github")
