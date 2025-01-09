## VSCode Settings

### How to Apply These Settings

1. Open the **Command Palette** with `Ctrl + Shift + P` (or `Cmd + Shift + P` on macOS).
2. Search for **"Preferences: Open Settings (JSON)"** and select it.
3. Copy and paste the following configuration into the JSON file.

```json
{
  "window.menuBarVisibility": "hidden",
  "window.commandCenter": false,
  "workbench.startupEditor": "newUntitledFile",
  "workbench.editor.editorActionsLocation": "hidden",
  "editor.tabSize": 2,
  "window.zoomLevel": 0.5,
  "editor.fontSize": 16,
  "editor.lineHeight": 1.8,
  "editor.rulers": [80, 120],
  "editor.wordWrap": "on",
  "editor.minimap.enabled": false,
  "editor.fontLigatures": true,
  "workbench.colorTheme": "Min Dark",
  "workbench.iconTheme": "symbols",
  "workbench.productIconTheme": "fluent-icons",
  "editor.fontFamily": "JetBrains Mono",
  "workbench.statusBar.visible": false,
  "workbench.editor.labelFormat": "short",
  "workbench.activityBar.location": "hidden",
  "workbench.editor.empty.hint": "hidden",
  "workbench.layoutControl.enabled": false,
  "editor.scrollbar.vertical": "hidden",
  "explorer.sortOrder": "foldersNestsFiles",
  "explorer.compactFolders": false,
  "explorer.confirmDragAndDrop": false,
  "symbols.hidesExplorerArrows": false,
  "editor.hideCursorInOverviewRuler": true,
  "editor.renderLineHighlight": "gutter",
  "terminal.integrated.fontSize": 14,
  "terminal.integrated.fontFamily": "JetBrainsMono Nerd Font",
  "terminal.integrated.profiles.windows": {
    "zsh": {
      "path": "C:\\Windows\\System32\\bash.exe",
      "args": ["-c", "zsh"],
      "icon": "star",
      "color": "terminal.ansiYellow",
      "overrideName": true
    }
  },
  "terminal.integrated.defaultProfile.windows": "zsh",
  "terminal.integrated.gpuAcceleration": "off",
  "terminal.integrated.env.osx": { "FIG_NEW_SESSION": "1" },
  "terminal.integrated.defaultProfile.osx": "fish",
  "terminal.integrated.showExitAlert": false,
  "javascript.suggest.autoImports": true,
  "typescript.suggest.autoImports": true,
  "javascript.updateImportsOnFileMove.enabled": "always",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "typescript.tsserver.log": "off",
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "always"
  },
  "[json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "vscode.json-language-features"
  },
  "[prisma]": {
    "editor.formatOnSave": true
  },
  "eslint.validate": [
    "javascript", "javascriptreact", "typescript", "typescriptreact"
  ],
  "tailwindCSS.experimental.classRegex": [
    ["tv\\(([^)]*)\\)", "[\"'`]([^\"'`]*).*?[\"'`]"]
  ],
  "files.associations": {
    ".env.*": "dotenv",
    ".prettierrc": "json",
    "*.css": "css"
  },
  "extensions.ignoreRecommendations": true,
  "update.showReleaseNotes": false,
  "update.mode": "start",
  "git.enableSmartCommit": true,
  "git.openRepositoryInParentFolders": "always",
  "security.workspace.trust.untrustedFiles": "newWindow",
  "security.promptForLocalFileProtocolHandling": false,
  "editor.parameterHints.enabled": false,
  "editor.accessibilitySupport": "off",
  "explorer.fileNesting.patterns": {
    "package.json": ".eslint*, prettier*, tsconfig*, vite*, pnpm-lock*, bun.lockb, nest*, eslint*, .prettier*",
    "tailwind.config.js": "tailwind.config*, postcss.config*",
    ".env.local": ".env*",
    ".env": ".env*"
  },
  "explorer.fileNesting.enabled": true,
  "files.exclude": {
    "**/CVS": true,
    "**/.DS_Store": true,
    "**/.hg": true,
    "**/.svn": true,
    "**/.git": true,
    ".vscode": true
  },
  "editor.suggestSelection": "recentlyUsedByPrefix",
  "explorer.confirmDelete": false
}
