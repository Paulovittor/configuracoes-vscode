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
"rocketseat.theme-omni"
]
}
```


Dentro de `settings.json` :

```json
{
  // editor
  "editor.wordWrap": "on",
  "editor.fontSize": 15, //tamanho da fonte
  "editor.lineHeight": 21, //tamanho do espaçamento entre linhas
  "editor.tabSize": 2,
  "editor.bracketPairColorization.enabled": true,
  "editor.guides.bracketPairs": true,
  "editor.minimap.enabled": false,
  "editor.formatOnSave": true,
  "editor.formatOnPaste": true,
  "files.autoSave": "afterDelay",

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
  "terminal.integrated.fontSize": 16,
  "terminal.integrated.profiles.windows": {
    "Git Bash": {
      "source": "Git Bash"
    }
  },
  "terminal.integrated.defaultProfile.windows": "Git Bash"
}

```

#EXTENSSÕES OPCIONAIS PARA MELHOR CUSTOMIZAÇÃO. <br>

:diamond_shape_with_a_dot_inside: Prettier - Code formatter <br>
:diamond_shape_with_a_dot_inside: Material icon theme <br>
:diamond_shape_with_a_dot_inside: Omni Theme <br>

obs: geralmente utilizando o @recommended nas extenssões do vs code.
