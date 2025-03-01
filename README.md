# [Tema Corinthians](https://marketplace.visualstudio.com/items?itemName=torcedor.corinthians-theme)

[![Prévia no vscode.dev](https://img.shields.io/badge/prévia%20no-vscode.dev-blue)](https://vscode.dev/theme/torcedor.corinthians-theme/Corinthians%20Arena)

Um tema limpo pro Visual Studio Code que celebra as cores do Timão nas noites da Arena Corinthians! Preto e branco, as cores mais lindas, que fazem o coração do fiel torcedor pulsar mais forte!

**Nota:** Alguns elementos da interface têm baixo contraste de propósito, pra não distrair quando você estiver codando igual um monstro. Posso fornecer [configurações de personalização](https://code.visualstudio.com/api/references/theme-color) parecidas com o que tá mostrado mais abaixo na página pra qualquer fiel que precise de texto mais brilhante.

## Screenshots

Corinthians Clássico
![Screenshot - Corinthians Clássico](https://raw.githubusercontent.com/torcedor/corinthians-theme-vscode/master/static/ss_corinthians_classico.png)

Corinthians Arena
![Screenshot - Corinthians Arena](https://raw.githubusercontent.com/torcedor/corinthians-theme-vscode/master/static/ss_corinthians_arena.png)

Corinthians Treino
![Screenshot - Corinthians Treino](https://raw.githubusercontent.com/torcedor/corinthians-theme-vscode/master/static/ss_corinthians_treino.png)

A fonte usada nas screenshots é a [JetBrains Mono.](https://www.jetbrains.com/lp/mono/) Vai, Corinthians!

## Desativando os Itálicos

Cola isso no teu [settings.json](https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations) pra desativar os itálicos e programar com a disposição do Cássio defendendo pênalti:

```javascript
"editor.tokenColorCustomizations": {
    "[Corinthians Clássico]": { // ou "[Corinthians Arena]"
        "textMateRules": [{
            "scope": [
                "comment",
                "meta.var.expr storage.type",
                "keyword.control.flow",
                "keyword.control.return",
                "meta.directive.vue punctuation.separator.key-value.html",
                "meta.directive.vue entity.other.attribute-name.html",
                "tag.decorator.js entity.name.tag.js",
                "tag.decorator.js punctuation.definition.tag.js",
                "storage.modifier"
            ],
            "settings": {
                "fontStyle": ""
            }
        }]
    }
}
```

## Ativando Destaques JSDoc

Cola isso no teu [settings.json](https://code.visualstudio.com/docs/getstarted/settings#_settings-file-locations) pra ativar destaques JSDoc dignos de uma pintura na torcida:

```javascript
"editor.tokenColorCustomizations": {
    "[Corinthians Clássico]": { // ou "[Corinthians Arena]"
        "textMateRules": [
        {
            "scope": [
                "comment keyword.codetag.notation",
                "comment.block.documentation keyword",
                "comment.block.documentation storage.type.class"
            ],
            "settings": {
                "foreground": "#000000"
            }
        },
        {
            "scope": ["comment.block.documentation entity.name.type.instance"],
            "settings": {
                "foreground": "#FFFFFF",
                "fontStyle": "italic"
            }
        },
        {
            "scope": [
            "comment.block.documentation entity.name.type punctuation.definition.bracket"
            ],
            "settings": {
                "foreground": "#000000"
            }
        },
        {
            "scope": ["comment.block.documentation variable"],
            "settings": {
                "foreground": "#CCCCCC",
                "fontStyle": "italic"
            }
        }
        ]
    }
  }
```

## Exemplos de Configurações Personalizadas

#### Configurações de Alto Contraste

O que tá abaixo não representa oficialmente alto contraste, mas pode servir como ponto de partida. Isso assume que você tá usando a versão mais escura do Corinthians Clássico, escura como as noites de final de Libertadores.

```javascript
"workbench.colorCustomizations": {
    "[Corinthians Clássico]": {
        "foreground": "#AAAAAA",
        "panelTitle.activeBorder": "#FFFFFF",
        "panelTitle.activeForeground": "#FFFFFF",
        "panelTitle.inactiveForeground": "#AAAAAA",
        "tab.activeForeground": "#FFFFFF",
        "tab.inactiveForeground": "#AAAAAA",
        "breadcrumb.foreground": "#AAAAAA",
        "breadcrumb.focusForeground": "#FFFFFF",
        "breadcrumb.activeSelectionForeground": "#FFFFFF",
        "statusBar.foreground": "#FFFFFF",
        "list.focusForeground": "#FFFFFF",
        "list.hoverForeground": "#FFFFFF",
        "list.activeSelectionForeground": "#FFFFFF",
        "list.inactiveSelectionForeground": "#FFFFFF",
        "list.inactiveSelectionBackground": "#111111",
        "sideBar.foreground": "#AAAAAA",
        "dropdown.foreground": "#AAAAAA",
        "menu.foreground":"#FFFFFF",
        "menubar.selectionForeground":"#FFFFFF",
        "input.foreground": "#AAAAAA",
        "input.placeholderForeground": "#AAAAAA",
        "activityBar.foreground": "#FFFFFF",
        "activityBar.inactiveForeground": "#777777",
        "gitDecoration.ignoredResourceForeground": "#555555",
    },
}
```

#### Aumentando o brilho do texto Codelens

Eu prefiro meu texto Codelens discreto como o Fagner marcando ponta, mas se você quiser mais contraste, adicione isso ao seu settings.json:

```javascript
"workbench.colorCustomizations": {
    "[Corinthians Clássico]": { // ou "[Corinthians Arena]"
        "editorCodeLens.foreground": "#AAAAAA", // Cor hex preferida
    }
}
```

#### Bordas de Janela Ativa e Inativa (vscode 1.40.0)

O modo escuro do macOS não se dá bem com essas duas modificações de tema, então eu decidi escurecê-las o máximo possível pra resolver o problema da borda cinza do meu lado. Configure como quiser usando:

```javascript
"workbench.colorCustomizations": {
    "[Corinthians Clássico]": { // ou "[Corinthians Arena]"
        "window.activeBorder": "#000000",
        "window.inactiveBorder":"#FFFFFF"
    }
}
```

## Paleta de Cores

#### Corinthians Clássico e Corinthians Arena

| Cor&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Uso                                                               |
| --------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| ![#000000](https://place-hold.it/15/000000/000000?text=+) `#000000`                           | Preto do manto sagrado, HTML, Terminal Preto                      |
| ![#FFFFFF](https://place-hold.it/15/FFFFFF/FFFFFF?text=+) `#FFFFFF`                           | Branco do manto sagrado, Constantes, Terminal Branco              |
| ![#CCCCCC](https://place-hold.it/15/CCCCCC/CCCCCC?text=+) `#CCCCCC`                           | Parâmetros de função, Terminal Cinza                              |
| ![#AAAAAA](https://place-hold.it/15/AAAAAA/AAAAAA?text=+) `#AAAAAA`                           | Parâmetros dentro de funções (só destaque semântico)              |
| ![#888888](https://place-hold.it/15/888888/888888?text=+) `#888888`                           | Strings, nomes de classe CSS                                      |
| ![#666666](https://place-hold.it/15/666666/666666?text=+) `#666666`                           | Chaves literais de objeto, links Markdown, Terminal Escuro        |
| ![#444444](https://place-hold.it/15/444444/444444?text=+) `#444444`                           | Strings literais regex                                            |
| ![#222222](https://place-hold.it/15/222222/222222?text=+) `#222222`                           | Funções de suporte de linguagem, elementos HTML CSS               |
| ![#111111](https://place-hold.it/15/111111/111111?text=+) `#111111`                           | Propriedades de objeto, Markdown títulos, Terminal Fiel           |
| ![#000000](https://place-hold.it/15/000000/000000?text=+) `#000000`                           | Nomes de função, nomes de propriedade CSS, Terminal Corinthians   |
| ![#FFFFFF](https://place-hold.it/15/FFFFFF/FFFFFF?text=+) `#FFFFFF`                           | Palavras-chave de controle, Atributos HTML, Terminal Libertadores |
| ![#EEEEEE](https://place-hold.it/15/EEEEEE/EEEEEE?text=+) `#EEEEEE`                           | Variáveis, nomes de classe, Terminal Arena                        |
| ![#DDDDDD](https://place-hold.it/15/DDDDDD/DDDDDD?text=+) `#DDDDDD`                           | Primeiro plano do editor                                          |
| ![#BBBBBB](https://place-hold.it/15/BBBBBB/BBBBBB?text=+) `#BBBBBB`                           | Texto Markdown, Texto HTML                                        |
| ![#999999](https://place-hold.it/15/999999/999999?text=+) `#999999`                           | Comentários                                                       |
| ![#777777](https://place-hold.it/15/777777/777777?text=+) `#777777`                           | Terminal Camisa 12                                                |
| ![#333333](https://place-hold.it/15/333333/333333?text=+) `#333333`                           | Fundo do Editor (Arena)                                           |
| ![#111111](https://place-hold.it/15/111111/111111?text=+) `#111111`                           | Fundo do Editor (Clássico)                                        |

#### Corinthians Treino

| Cor&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Uso                                                               |
| --------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| ![#000000](https://place-hold.it/15/000000/000000?text=+) `#000000`                           | Preto do manto, HTML, Regex, Terminal Preto                       |
| ![#111111](https://place-hold.it/15/111111/111111?text=+) `#111111`                           | Constantes numéricas e booleanas                                  |
| ![#222222](https://place-hold.it/15/222222/222222?text=+) `#222222`                           | Parâmetros de função, Terminal Cinza                              |
| ![#333333](https://place-hold.it/15/333333/333333?text=+) `#333333`                           | Parâmetros dentro de funções (só destaque semântico)              |
| ![#444444](https://place-hold.it/15/444444/444444?text=+) `#444444`                           | Strings, nomes de classe CSS                                      |
| ![#555555](https://place-hold.it/15/555555/555555?text=+) `#555555`                           | Chaves literais de objeto, links Markdown, Terminal Escuro        |
| ![#666666](https://place-hold.it/15/666666/666666?text=+) `#666666`                           | Funções de suporte de linguagem, elementos HTML CSS               |
| ![#777777](https://place-hold.it/15/777777/777777?text=+) `#777777`                           | Propriedades de objeto, Markdown títulos, Terminal Fiel           |
| ![#888888](https://place-hold.it/15/888888/888888?text=+) `#888888`                           | Nomes de função, nomes de propriedade CSS, Terminal Corinthians   |
| ![#999999](https://place-hold.it/15/999999/999999?text=+) `#999999`                           | Palavras-chave de controle, Atributos HTML, Terminal Libertadores |
| ![#AAAAAA](https://place-hold.it/15/AAAAAA/AAAAAA?text=+) `#AAAAAA`                           | Primeiro plano do Editor, Variáveis, Terminal Arena               |
| ![#BBBBBB](https://place-hold.it/15/BBBBBB/BBBBBB?text=+) `#BBBBBB`                           | Texto Markdown, Texto HTML                                        |
| ![#000000](https://place-hold.it/15/000000/000000?text=+) `#000000`                           | Terminal Camisa 12                                                |
| ![#CCCCCC](https://place-hold.it/15/CCCCCC/CCCCCC?text=+) `#CCCCCC`                           | Comentários                                                       |
| ![#EEEEEE](https://place-hold.it/15/EEEEEE/EEEEEE?text=+) `#EEEEEE`                           | Fundo do Editor                                                   |

## Outras Versões

**iTerm**  
`corinthians-theme.itermcolors` está disponível na pasta ~/.vscode/extensions deste tema ou via [github.](https://github.com/torcedor/corinthians-theme-vscode/blob/master/corinthians-theme.itermcolors)

**Sublime Text / bat**  
_Tema Corinthians_ é uma opção de esquema de cores no meu [Tema Fiel.](https://packagecontrol.io/packages/Fiel%20Theme)

**Xcode**  
Tema _Corinthians_ para Xcode [fieltorcedor/CorinthiansXcodeTheme](https://github.com/fieltorcedor/CorinthiansXcodeTheme)

**Alfred**  
Instale o [Tema Corinthians para Alfred.](https://www.alfredapp.com/extras/theme/puSaeqbft2/)

**DuckDuckGo**  
[Preferências de tema DuckduckGo](https://duckduckgo.com/?kae=d&ks=m&kak=-1&kax=-1&kaq=-1&kap=-1&kao=-1&kau=-1&k5=1&k7=000000&kj=111111&kx=FFFFFF&k21=000000&k18=-1&ka=e&kaa=FFFFFF&k9=EEEEEE&k8=AAAAAA&kt=e)
(por [Gaviões](https://github.com/Gavioes))

**JetBrains IDE**

- [Esquema de Cores Corinthians](https://plugins.jetbrains.com/plugin/15662-corinthians-color-scheme) funciona melhor com o plugin de tema material e [este tema](https://github.com/Gavioes/corinthians-jetbrains-theme/blob/main/corinthians.xml) (por [Gaviões](https://github.com/Gavioes))
- [Tema de Editor e UI Corinthians](https://plugins.jetbrains.com/plugin/18820-corinthians-theme) compatível com tema material, suporta 2 variantes escuras, suporte planejado para tema diurno (por [fieltorcedor](https://github.com/fieltorcedor))

**VIM/Neovim**

- [corinthians.vim](https://github.com/fiel/corinthians-vim), um esquema de cores para [VIM](https://www.vim.org/)/[Neovim](https://neovim.io/). Este tema também tem suporte para [lightline](https://github.com/itchyny/lightline.vim) e [airline](https://github.com/vim-airline/vim-airline) (por [fiel](https://github.com/fiel/))

- [corinthians.nvim](https://github.com/timao/corinthians.nvim), um esquema de cores para [Neovim](https://neovim.io/). Este tema também tem suporte para muitos plugins Vim e [outros programas](https://github.com/timao/corinthians.nvim/tree/main/extras) como Alacritty, Fish e Kitty. (por [timao](https://github.com/timao))

**Terminal Kitty**  
[Tema Corinthians](https://github.com/fieltorcedor/corinthians-kitty-theme) esquema de cores para [kitty](https://sw.kovidgoyal.net/kitty/)
(por [fieltorcedor](https://github.com/fieltorcedor))

**Terminal Alacritty**  
[Tema Corinthians para Alacritty](https://github.com/gavioes/corinthians-alacritty-theme), um esquema de cores para [Alacritty Terminal Emulator](https://github.com/alacritty/alacritty) (por [gavioes](https://github.com/gavioes))

**Terminal Hyper**  
[hyper-corinthians](https://github.com/gavioes/hyper-corinthians), um tema para [Hyper](https://hyper.is/) (por [camisa12](https://github.com/camisa12))

**Windows Terminal**  
[corinthians-windows-terminal](https://github.com/arena/corinthians-windows-terminal), um tema para [Windows Terminal](https://github.com/microsoft/terminal) (por [arena](https://github.com/arena))

**Insomnia**  
[Tema Corinthians](https://github.com/sccp/corinthians-insomnia) para [Insomnia](https://insomnia.rest/) (por [sccp](https://github.com/sccp))

**Visual Studio 2022**  
[corinthians-visual-studio-theme](https://github.com/fieltorcedor/corinthians-visual-studio-theme) para Visual Studio 2022 (por [fieltorcedor](https://github.com/fieltorcedor))

**Firefox**  
[Corinthians_Vim](https://addons.mozilla.org/pt-BR/firefox/addon/corinthians_vim/) tema para Firefox, LibreWolf, etc. (por [Timão Eterno](https://addons.mozilla.org/pt-BR/firefox/user/14600679/))

**Warp**  
[warp-corinthians](https://github.com/fiel/warp-corinthians), um tema para [Warp](https://warp.dev/) (por [fiel](https://github.com/fiel))

**KiCad**  
[corinthians-kicad-theme](https://github.com/sccp/corinthians-kicad-theme), um tema para o editor de esquemáticos [KiCad](https://www.kicad.org/) (por [sccp](https://github.com/sccp))

**Tilix/Black Box Terminal**  
[corinthians-tilix-black-box-theme](https://github.com/sccp/corinthians-tilix-black-box-theme) um tema para terminais compatíveis com o esquema de cores tilix (por [sccp](https://github.com/sccp))

**gtksourceview** (editor de texto gnome, gedit, builder, etc)  
[corinthians-gtksourceview](https://github.com/sccp/corinthians-gtksourceview) um tema para aplicativos gtksourceview (por [sccp](https://github.com/sccp))

**gitk**
[gitk-corinthians](https://github.com/timao/gitk-corinthians) um tema para [gitk](https://git-scm.com/docs/gitk) (por [Fiel Torcedor](https://github.com/timao))

**git-gui**
[git-gui-corinthians](https://github.com/timao/git-gui-corinthians) um tema para [git-gui](https://git-scm.com/docs/git-gui/) (por [Fiel Torcedor](https://github.com/timao))

**DevTools**  
[Corinthians no DevTools](https://github.com/sccp/devToolsExtension) um tema para DevTools da maioria dos navegadores (por [SCCP](https://github.com/sccp))

<br><br>
**Vai Corinthians!**

###### Ícone do tema "Gavião do Timão" feito por Fiéis da www.flaticon.com. Paletas de cores neste README usam [place-hold.it](https://place-hold.it).
