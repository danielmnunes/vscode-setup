# vscode-setup

Configurações versionadas para perfis de desenvolvimento no Visual Studio Code.

## Perfis disponíveis

| Perfil | Configuração | Extensões |
|---|---|---|
| Java moderno + Spring | [settings.json](profiles/java-spring/settings.json) | [extensions.txt](profiles/java-spring/extensions.txt) |
| Go | [settings.json](profiles/golang/settings.json) | [extensions.txt](profiles/golang/extensions.txt) |
| Rust | [settings.json](profiles/rust/settings.json) | [extensions.txt](profiles/rust/extensions.txt) |
| Frontend com Vue.js | [settings.json](profiles/vue-frontend/settings.json) | [extensions.txt](profiles/vue-frontend/extensions.txt) |
| Python | [settings.json](profiles/python/settings.json) | [extensions.txt](profiles/python/extensions.txt) |

Consulte [profiles/README.md](profiles/README.md) para criar os perfis e aplicar as configurações.

As preferências evitam caminhos locais de JDK, Python, Go e Rust. Versões de runtime e regras de build devem ser definidas por cada projeto e ambiente.
