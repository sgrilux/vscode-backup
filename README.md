# vscode-backup

How I backup and restore my Visual Studio Code extensions and settings.

## Backup

### settings

Settings are stored in `settings.json` underneath `~/Library/Application\ Support/Code/User`

### exetensions

```shell
code --list-extensions > vscode.extensions.txt
```

## Restore

```shell
cat vscode.extensions.txt | xargs -n 1 code --install-extension
```

```
cp settings.json ~/Library/Application\ Support/Code/User/
```
