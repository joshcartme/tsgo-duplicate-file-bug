If you have a js and ts file with the same name, `rootNames` in the computed config ends up with a `""` entry. This seems to hang the server, it never starts responding.

Output from the VSCode extension:

```
Resolved to /home/repro/.vscode-server/extensions/typescriptteam.native-preview-0.20250529.1-linux-x64/lib/tsgo
Starting language server...
Info 0    [14:36:15.239] currentDirectory:: /home/repro/development/tsgo-duplicate-file-bug useCaseSensitiveFileNames:: true
Info 1    [14:36:15.240] libs Location:: /home/repro/.vscode-server/extensions/typescriptteam.native-preview-0.20250529.1-linux-x64/lib
Info 2    [14:36:15.244] getConfigFileNameForFile:: File: /home/repro/development/tsgo-duplicate-file-bug/index.ts ProjectRootPath: :: Result: /home/repro/development/tsgo-duplicate-file-bug/tsconfig.json
Info 3    [14:36:15.244] Creating KindConfiguredProject: /home/repro/development/tsgo-duplicate-file-bug/tsconfig.json, currentDirectory: /home/repro/development/tsgo-duplicate-file-bug
Info 4    [14:36:15.244] Config: /home/repro/development/tsgo-duplicate-file-bug/tsconfig.json : {
      "options": {
        "allowJs": true,
        "configFilePath": "/home/repro/development/tsgo-duplicate-file-bug/tsconfig.json"
      },
      "projectReferences": [],
      "rootNames": [
        "/home/repro/development/tsgo-duplicate-file-bug/index.ts",
        "",
        "/home/repro/development/tsgo-duplicate-file-bug/lib.ts"
      ]
    }
```
