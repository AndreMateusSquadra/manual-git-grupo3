# Instalação e Configuração do Git

## Onde Baixar e Instalar

### Windows

1. Acesse o site oficial do Git: https://git-scm.com/download/win
2. O download deve começar automaticamente
3. Execute o instalador baixado
4. Durante a instalação, você pode manter as opções padrão
5. Após a instalação, abra o Git Bash ou o Prompt de Comando para verificar a instalação

### Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install git
```

### macOS

1. Se você tem o Xcode instalado, o Git já vem incluído
2. Alternativamente, você pode instalar via Homebrew:
```bash
brew install git
```

## Configuração Inicial do Git

Após a instalação, é importante configurar suas credenciais básicas. Abra o terminal (ou Git Bash no Windows) e execute os seguintes comandos:

### Configurar Nome de Usuário

```bash
git config --global user.name "Seu Nome"
```

### Configurar Email

```bash
git config --global user.email "seu.email@exemplo.com"
```

### Verificar Configurações

Para ver todas as suas configurações atuais:

```bash
git config --list
```

## Configurações Adicionais Recomendadas

### Configurar o Editor Padrão

```bash
# Para VS Code
git config --global core.editor "code --wait"

# Para Vim
git config --global core.editor "vim"

# Para Nano
git config --global core.editor "nano"
```

### Configurar o Branch Padrão

```bash
git config --global init.defaultBranch main
```

## Verificando a Instalação

Para confirmar que o Git foi instalado corretamente:

```bash
git --version
```

Você deve ver algo como: `git version 2.x.x`

**Nota:** Certifique-se de reiniciar o terminal após a instalação para que o comando `git` seja reconhecido.

## Primeiros Passos

1. Crie uma pasta para seus projetos:
```bash
mkdir meus-projetos
cd meus-projetos
```

2. Inicialize um repositório Git:
```bash
git init
```

3. Verifique o status:
```bash
git status
```

## Dicas de Configuração

### Aliases Úteis

Você pode criar atalhos (aliases) para comandos comuns:

```bash
# Criar um alias para 'git status'
git config --global alias.st status

# Criar um alias para 'git checkout'
git config --global alias.co checkout

# Criar um alias para 'git branch'
git config --global alias.br branch
```

### Configuração de Cores

Para melhorar a legibilidade:

```bash
git config --global color.ui true
```

## Solução de Problemas Comuns

### Erro de Permissão

Se você encontrar erros de permissão no Windows:
1. Execute o Git Bash como administrador
2. Verifique as permissões da pasta do projeto

### Erro de Configuração

Se as configurações não estiverem sendo salvas:
1. Verifique se você tem permissões de escrita
2. Tente usar `--system` em vez de `--global`

## Próximos Passos

Agora que você tem o Git instalado e configurado, você está pronto para começar a usar os comandos básicos do Git, que serão abordados no próximo módulo. 