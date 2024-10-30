# equation-solver-language

VS Code extension for the [Equation Solver Language](https://github.com/c-chapellier/equation-solver).

Goal is to support syntax highlighting and error/warning messages based on the language server (to be implemented). 

## Getting Started

1. Clone this repo
2. Run `npm install` from the repo root.
3. Press `F5` to open a new window with your extension loaded.

## Anatomy

```
.
├── .vscode
│   ├── launch.json         // Tells VS Code how to launch our extension
│   └── tasks.json          // Tells VS Code how to build our extension
├── client
│   ├── src
│   │   └── extension.ts    // Code to tell VS Code how to run our language server
├── server
│   ├── src
│   │   └── server.ts       // Language server code
├── syntaxes
│   ├── es.tmLanguage.json  // Tells VS Code how to tokenize the language
│   └── es.tmLanguage.yml   // Used to generate the previous json file
├── language-configuration.json // this is the language configuration, defining the tokens that are used for comments and brackets.
├── package.json            // Top-level manifest
├── README.md
└── tsconfig.json           // Top-level TypeScript config
```

## Update the grammar

1. Install the tool: `npm install js-yaml --save-dev`
2. Convert yaml to json: `npx js-yaml syntaxes/es.tmLanguage.yml > syntaxes/es.tmLanguage.json`

## Sources

* [Semanticart - Minimal Language Server Extension](https://github.com/semanticart/minimum-viable-vscode-language-server-extension)
* [VSCode - Syntax Highlighting](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide)
* [TextMate Grammar](https://macromates.com/manual/en/language_grammars)
