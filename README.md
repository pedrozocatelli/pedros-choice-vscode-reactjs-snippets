<h1 align="center">
   Pedro's Choice - ReactJS Snippets
</h1>

This extension contains a selections of the best ReactJS Snippets and commands chosen by Pedro.


## React

|  Prefix | Method                                              |
| ------: | --------------------------------------------------- |
|  `imp→` | `import moduleName from 'module'`                   |
|  `imn→` | `import 'module'`                                   |
|  `imd→` | `import { destructuredModule } from 'module'`       |
|  `ime→` | `import * as alias from 'module'`                   |
|  `ima→` | `import { originalName as aliasName} from 'module'` |
|  `exp→` | `export default moduleName`                         |
|  `exd→` | `export { destructuredModule } from 'module'`       |
|  `exa→` | `export { originalName as aliasName} from 'module'` |
|  `enf→` | `export const functionName = (params) => { }`       |
|  `edf→` | `export default (params) => { }`                    |
|  `met→` | `methodName = (params) => { }`                      |
|  `fre→` | `arrayName.forEach(element => { }`                  |
|  `fof→` | `for(let itemName of objectName { }`                |
|  `fin→` | `for(let itemName in objectName { }`                |
| `anfn→` | `(params) => { }`                                   |
|  `nfn→` | `const functionName = (params) => { }`              |
|  `dob→` | `const {propName} = objectToDescruct`               |
|  `dar→` | `const [propName] = arrayToDescruct`                |
|  `sti→` | `setInterval(() => { }, intervalTime`               |
|  `sto→` | `setTimeout(() => { }, delayTime`                   |
| `prom→` | `return new Promise((resolve, reject) => { }`       |
| `cmmb→` | `comment block`                                     |
|   `cp→` | `const { } = this.props`                            |
|   `cs→` | `const { } = this.state`                            |

## Add to your project

There are 2 ways you can add Pedro's Choice - Keymap to your project:

#### By command
Launch VS Code Quick Open (`Ctrl+P`), paste `ext install pedroschoice.pedros-choice-vscode-keybindings`, and press enter.

#### By the Extension Marketplace
Launch VS Code Extension Marketplace (Ctrl+Shift+X), search for `Pedro's Choice`, and look for the best looking bald dude in the store.

## Contributing
### How do I contribute?

If you have a sugestion of an awesome shortcut, let me know.

1. Head over to the [GitHub repository](https://github.com/pedrozocatelli/pedros-choice-vscode-keybindings). 
2. Open the [`package.json` file](https://github.com/pedrozocatelli/pedros-choice-vscode-keybindings/blob/master/package.json). 
3. Add a JSON object to [`contributes.keybindings`](https://github.com/pedrozocatelli/pedros-choice-vscode-keybindings/blob/master/package.json#L199) as seen below. 
4. Open a pull request. 

```json
{
   "mac": "<keyboard shortcut for mac>",
   "win": "<keyboard shortcut for windows>",
   "linux": "<keyboard shortcut for linux>",
   "key": "<default keyboard shorcut>",
   "command": "<which command it will trigger>",
   "when": "<when it should trigger>"
}
```

## License
[MIT](LICENSE.md)