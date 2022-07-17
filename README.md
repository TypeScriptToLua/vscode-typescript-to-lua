[![](https://img.shields.io/visual-studio-marketplace/v/typescript-to-lua.vscode-typescript-to-lua?color=g&label=Visual%20Studio%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=typescript-to-lua.vscode-typescript-to-lua)

A Visual Studio Code extension that adds [TypeScriptToLua](https://typescripttolua.github.io)
support for TypeScript using the
[TypeScript TypeScriptToLua Language Service plugin](https://github.com/TypeScriptToLua/typescript-tstl-plugin).

## Usage

This extension activates automatically when project's `tsconfig.json` file has `"tstl"` key.

## Features

### TypeScriptToLua Diagnostics

Sometimes, code that would normally be valid in JavaScript/TypeScript would be invalid when transpiling to Lua. The TSTL extension will immediately warn you when this is the case, so that you discover it at writing-time rather than at compile-time. For example:

![](/docs/diagnostics.png)

### Automatic tsconfig.json Schema

- In most popular IDEs, you can specify a "$schema" key at the top of a JSON file. Doing this activates auto-complete and field validation, which makes working with the JSON much easier.
- One extra feature of VSCode is that if you happen to be working in a `tsconfig.json` file without an explicitly defined "$schema" key, the editor will automatically use [the standard tsconfig schema](https://json.schemastore.org/tsconfig).
- If this extension detects a "tstl" key in the "tsconfig.json" file, then it will automatically swap the schema to [one that includes the possible values for the "tstl" key](https://github.com/TypeScriptToLua/TypeScriptToLua/blob/master/tsconfig-schema.json). This allows for auto-completing the TSTL properties:

![](/docs/tsconfig-schema.png)
