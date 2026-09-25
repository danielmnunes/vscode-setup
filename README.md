# vscode-setup

Configurações versionadas para o Visual Studio Code.

## Configuração global de aparência

- [settings.json](settings.json) define fonte, ligaduras, tema de cores **One Dark Pro** e ícones de arquivos/pastas **Material Icon Theme**.
- [global-extensions.txt](global-extensions.txt) lista as duas extensões necessárias para o tema e os ícones.

Instale no sistema operacional a fonte que deseja usar. O VS Code escolhe a primeira fonte disponível na ordem: JetBrains Mono, Fira Code e Cascadia Code.

Para aplicar:

1. Abra **Preferences: Open User Settings (JSON)** e incorpore as configurações de [settings.json](settings.json).
2. Selecione **Apply Setting to all Profiles** para as configurações de aparência, caso use mais de um perfil.
3. Instale as extensões de [global-extensions.txt](global-extensions.txt) e escolha **Apply Extension to all Profiles** para cada uma.

No terminal, a lista de extensões pode ser instalada no perfil atual com:

```sh
while IFS= read -r extension; do
  [ -z "$extension" ] || code --install-extension "$extension"
done < global-extensions.txt
```

O arquivo na raiz é um modelo: o VS Code não o carrega automaticamente como configuração global.

## Perfis por linguagem

| Perfil | Configuração | Extensões |
|---|---|---|
| Java moderno + Spring | [settings.json](profiles/java-spring/settings.json) | [extensions.txt](profiles/java-spring/extensions.txt) |
| Go | [settings.json](profiles/golang/settings.json) | [extensions.txt](profiles/golang/extensions.txt) |
| Rust | [settings.json](profiles/rust/settings.json) | [extensions.txt](profiles/rust/extensions.txt) |
| Frontend com Vue.js | [settings.json](profiles/vue-frontend/settings.json) | [extensions.txt](profiles/vue-frontend/extensions.txt) |
| Python | [settings.json](profiles/python/settings.json) | [extensions.txt](profiles/python/extensions.txt) |

Consulte [profiles/README.md](profiles/README.md) para criar os perfis e aplicar suas configurações.
