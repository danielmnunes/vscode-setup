# Como aplicar os perfis

Este repositório mantém os arquivos de configuração e as listas de extensões de cada perfil. As pastas aqui são modelos versionados; os perfis pessoais do VS Code ficam no diretório de usuário da instalação.

## Aplicar um perfil

1. Abra o VS Code e execute **Profiles: Create Profile...** na Paleta de Comandos.
2. Crie um perfil vazio com o nome desejado, por exemplo **Java + Spring**.
3. No terminal, instale as extensões do perfil. Exemplo para Java + Spring:

   ```sh
   while IFS= read -r extension; do
     [ -z "$extension" ] || code --profile "Java + Spring" --install-extension "$extension"
   done < profiles/java-spring/extensions.txt
   ```

   Troque o nome do perfil e o caminho da lista para outro conjunto. A opção `--profile` instala as extensões no perfil indicado.

4. Ative o perfil na janela atual. Execute **Preferences: Open User Settings (JSON)** e copie o conteúdo do `settings.json` correspondente para as configurações desse perfil.

No Windows, execute os comandos no PowerShell ou Git Bash depois de instalar o comando `code` no PATH. O comando da etapa 3 está escrito para shells Bash, incluindo WSL e Git Bash.

## Perfis nativos exportados

O VS Code exporta um perfil nativo como arquivo `.code-profile` pelo editor de Perfis. Os arquivos neste repositório mantêm as configurações e extensões em formatos fáceis de revisar no Git; aplique-os pelo processo acima. Para gerar um `.code-profile` depois de configurar um perfil, abra **Profiles: Show Profiles**, escolha **Export Profile...** e salve o arquivo exportado.

## Escolhas e limites

- As listas mantêm o conjunto de extensões focado em suporte de linguagem, testes, depuração e ferramentas comuns do ecossistema.
- A extensão Python instala como dependências opcionais o Pylance, Python Debugger e Python Environments; por isso elas não são repetidas nas listas.
- O perfil Java + Spring não fixa um JDK. A extensão Java usa um JRE próprio para seu servidor de linguagem em plataformas suportadas; o JDK do projeto deve ser configurado pelo próprio projeto ou pelo ambiente.
- Os perfis não instalam runtimes nem dependências do projeto. Instale JDK, Go, Rust/Cargo, Node.js e Python separadamente conforme sua plataforma e projeto.
- As configurações de formatador podem precisar de ajustes para obedecer às regras já adotadas pelo projeto.
