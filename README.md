# vscode-setup

Configurações versionadas para o Visual Studio Code.

## Configuração global de fontes

O arquivo [settings.json](settings.json) configura editor e terminal com uma lista de fallback nesta ordem: JetBrains Mono, Fira Code e Cascadia Code. Instale no sistema operacional a fonte que deseja usar. A primeira fonte disponível na lista será selecionada.

Para aplicar globalmente, abra **Preferences: Open User Settings (JSON)** no VS Code e copie as quatro configurações de [settings.json](settings.json). O arquivo na raiz do repositório é um modelo e não é carregado automaticamente como configuração global.

## Perfis disponíveis

| Perfil | Configuração | Extensões |
|---|---|---|
| Java moderno + Spring | [settings.json](profiles/java-spring/settings.json) | [extensions.txt](profiles/java-spring/extensions.txt) |
| Go | [settings.json](profiles/golang/settings.json) | [extensions.txt](profiles/golang/extensions.txt) |
| Rust | [settings.json](profiles/rust/settings.json) | [extensions.txt](profiles/rust/extensions.txt) |
| Frontend com Vue.js | [settings.json](profiles/vue-frontend/settings.json) | [extensions.txt](profiles/vue-frontend/extensions.txt) |
| Python | [settings.json](profiles/python/settings.json) | [extensions.txt](profiles/python/extensions.txt) |

Consulte [profiles/README.md](profiles/README.md) para criar os perfis e aplicar as configurações.
