# CUSTOMIZANDO O VS CODE ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
PRIMEIRAMENTE VAMOS CRIAR UMA ESTRUTURA DE DESENVOLVIMENTO USANDO O VITE E NODE.JS

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) <br>
Primeiramente deve-se instalar o NODE.js pois o VITE é baseado nesta ferramenta por este link: https://nodejs.org/en baixando a versao LTS que será instalado automaticamente junto com o NPM (node package manage).

![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white) <br>
Para a instalação do Vite é necessário faze um primeiro programa teste:
1. Crie uma pasta para armazenar o projeto e a estrutura de desenvolvimento que o vite irá gerar=.
2. Abra o terminal dentro desta página e utilizando os comando npm digite o código: <em><strong>`npm create vite@latest`</strong></em>
3. O terminal irá propor instalar suporte ao vite, clicar em "y" para sim e será instalado
4. Após instalado, o terminal irá pedir o nome do projeto teste, depois o framework que irá ser utilizado no projeto e após isso a linguagem de programação: javascript ou typescript
5. A estrutura de desenvolvimento esta criada.

# CUSTOMIZAÇÃO
1. Abrindo o projeto no vs code, deve-se criar a pasta especial para a curstomização da IDE com nome: <em><strong>`.vscode`</strong></em> :file_folder:
2. Dentro desta pasta deve-se criar dois arquivos: `extensions.json` e `settings.json`

#CÓDIGOS <br>
Dentro de `extensions.json` :

```json
{
  "recommendations": [
    "esbenp.prettier-vscode",
    "PKief.material-icon-theme",
    "rocketseat.theme-omni",
    "pranaygp.vscode-css-peek",
    "kisstkondoros.vscode-gutter-preview",
    "vincaslt.highlight-matching-tag",
    "anteprimorac.html-end-tag-labels",
  ]
}
```


Dentro de `settings.json` :

```json
{
  // editor
  "editor.wordWrap": "on",
  "editor.fontSize": 12,
  "editor.lineHeight": 21,
  "editor.tabSize": 2,
  "editor.fontWeight": 450,
  "editor.fontFamily": "Fira Code",
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": true,
  "editor.minimap.enabled": false,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "files.autoSave": "afterDelay",
  //editando cor de fundo do tema omni
  "workbench.colorCustomizations": {
    "editor.background": "#0f0f0f"
},


  // explorer
  "explorer.compactFolders": false,

  // workbench
  "workbench.editor.enablePreview": false,
  "workbench.iconTheme": "material-icon-theme",
  "workbench.colorTheme": "Omni",

  // prettier
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "prettier.enable": true,
  "prettier.singleQuote": false,
  "prettier.tabWidth": 2,
  "prettier.semi": false,

  // terminal
  "terminal.integrated.fontSize": 12,
  "terminal.integrated.profiles.windows": {
    "Git Bash": {
      "source": "Git Bash"
    }
  },
  "terminal.integrated.defaultProfile.windows": "Git Bash"
}

```

# EXTENSSÕES OPCIONAIS PARA MELHOR CUSTOMIZAÇÃO. <br>

:diamond_shape_with_a_dot_inside: Material icon theme: serve para melhorar os ícones dos arquivos. <br>
:diamond_shape_with_a_dot_inside: Erros leans: serve para marcar os erros in line. <br>
:diamond_shape_with_a_dot_inside: O tema Omni muda a aparencia do vs code. <br>

Como definido na extensions.json, pesquisando com @recommedations, todas essas extenssões apareceção para serem instaladas, icluindo notificações de instalação.


# Customizando o tema omni com editor.tokenColorCustomizations.

Deve-se abrir as opções em `arquivo`, ir em `preferencias` e depois em `configurações` pesquisar por "token" e na opção `Editor: Token Color Customizations` clicar em `editar em: settings.json` neste arquivo, dentro de `editor.tokenColorCustomizations` por o seguinte código:

```json
"editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": ["comment", "punctuation.definition.comment"],
        "settings": {
          "foreground": "#44794d" // Cor para comentários e símbolos de comentários
        }
      },
      {
        "scope": [
          "entity.name.tag.html",
          "punctuation.definition.tag.begin.html",
          "punctuation.definition.tag.end.html"
        ],
        "settings": {
          "foreground": "#0492cf" // Cor para tags HTML e símbolos < e >
        }
      },
      {
        "scope": ["entity.other.attribute-name.html"],
        "settings": {
          "foreground": "#95d4d4" // Cor para atributos HTML
        }
      },
      {
        "scope": ["string.quoted.double.html"],
        "settings": {
          "foreground": "#c48a58" // Cor para valores em aspas duplas HTML
        }
      },
      {
        "scope": [
          "keyword.operator.assignment.html",
          "punctuation.separator.key-value.html"
        ],
        "settings": {
          "foreground": "#8bc5c5" // Cor para o símbolo = em atributos
        }
      },
      {
        "scope": [
          "punctuation.definition.string.begin.html",
          "punctuation.definition.string.end.html"
        ],
        "settings": {
          "foreground": "#c48a58" // Cor para as aspas duplas dos valores dos atributos
        }
      },
      {
        "scope": [
          "support.type.property-name.css" // Propriedades CSS
        ],
        "settings": {
          "foreground": "#1f96ce" // Cor para propriedades CSS
        }
      },
      {
        "scope": [
          "support.constant.property-value.css" // Valores CSS
        ],
        "settings": {
          "foreground": "#00FF00" // Cor para valores CSS
        }
      },
      {
        "scope": [
          "entity.name.tag.css" // Seletores CSS
        ],
        "settings": {
          "foreground": "#FFA500" // Cor para seletores CSS
        }
      },
      {
        "scope": [
          "punctuation.separator.key-value.css" // Símbolo : em CSS
        ],
        "settings": {
          "foreground": "#9cdbf8" // Cor para símbolo :
        }
      },
      {
        "scope": [
          "constant.numeric.css" // Números em CSS
        ],
        "settings": {
          "foreground": "#faf4ea" // Cor para números
        }
      },

      // Personalizações para strings JavaScript (entre aspas)
      {
        "scope": ["string.quoted.single.js", "string.quoted.double.js"],
        "settings": {
          "foreground": "#bdb43d" // Cor para strings JavaScript
        }
      },

      // Personalizações para valores JavaScript
      {
        "scope": [
          "constant.language.js",
          "variable.language.js",
          "variable.other.js"
        ],
        "settings": {
          "foreground": "#00FF00" // Cor para valores JavaScript
        }
      },


      //CUSTOMIZANDO OS ARQUIVOS JSON
      {
        "scope": ["string.quoted.single.json", "string.quoted.double.json"],
        "settings": {
          "foreground": "#c7a865" // Cor para strings JavaScript
        }
      }

    ]
  }
```

No código acima terá toda as configurações de cores das sintaxes html, css e algumas de javascrips que poderão ser customizadas dentro desse proprio arquivo.
Juntamente com esse, no arquivo settings.json pode-se customizar o background-color do tema omni com o codigo abaixo:

```json
  "workbench.colorCustomizations": {
    "editor.background": "#181717"
},
```


