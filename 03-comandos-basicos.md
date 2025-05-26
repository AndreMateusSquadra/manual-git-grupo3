# Comandos Básicos do Git

Este guia apresenta os comandos mais fundamentais do Git, essenciais para o dia a dia do desenvolvimento.

## Inicializando um Repositório

### git init

Cria um novo repositório Git em um diretório:

```bash
# Navegue até a pasta do seu projeto
cd meu-projeto

# Inicialize o repositório
git init
```

Após executar `git init`, uma pasta `.git` é criada, contendo todos os arquivos necessários para o controle de versão.

## Verificando o Estado

### git status

Mostra o estado atual do seu repositório:

```bash
git status
```

Exemplo de saída:
```
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md
        modified:   arquivo.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        novo-arquivo.txt
```

## Adicionando Arquivos

### git add

Adiciona arquivos à área de preparação (staging area):

```bash
# Adicionar um arquivo específico
git add arquivo.txt

# Adicionar todos os arquivos modificados
git add .

# Adicionar arquivos com um padrão específico
git add *.txt
```

## Criando Commits

### git commit

Salva as mudanças no histórico do repositório:

```bash
# Commit com mensagem
git commit -m "Adiciona nova funcionalidade"

# Commit com mensagem detalhada
git commit -m "Título do commit" -m "Descrição detalhada das mudanças"
```

Dicas para boas mensagens de commit:
- Use verbos no imperativo
- Seja específico e conciso
- Explique o "porquê" quando necessário

## Visualizando o Histórico

### git log

Mostra o histórico de commits:

```bash
# Histórico básico
git log

# Histórico com uma linha por commit
git log --oneline

# Histórico com gráfico de branches
git log --graph --oneline --all
```

## Exemplo Prático

Vamos ver um exemplo completo de fluxo de trabalho:

```bash
# 1. Criar um novo arquivo
echo "# Meu Projeto" > README.md

# 2. Verificar o status
git status

# 3. Adicionar o arquivo
git add README.md

# 4. Criar o primeiro commit
git commit -m "Adiciona README inicial"

# 5. Fazer uma modificação
echo "Nova linha" >> README.md

# 6. Verificar as mudanças
git status

# 7. Adicionar e commitar a mudança
git add README.md
git commit -m "Atualiza README com nova informação"
```

## Boas Práticas

1. **Commits Atômicos**
   - Faça commits pequenos e focados
   - Cada commit deve representar uma mudança lógica

2. **Mensagens Claras**
   - Use mensagens descritivas
   - Siga um padrão consistente

3. **Verificação Regular**
   - Use `git status` frequentemente
   - Verifique o histórico com `git log`

## Comandos Adicionais Úteis

### git diff

Mostra as diferenças entre arquivos:

```bash
# Ver mudanças não adicionadas
git diff

# Ver mudanças já adicionadas
git diff --staged
```

### git restore

Desfaz mudanças em arquivos:

```bash
# Desfaz mudanças em um arquivo
git restore arquivo.txt

# Desfaz todas as mudanças
git restore .
```

### git rm

Remove arquivos do Git:

```bash
# Remove arquivo e adiciona a remoção ao staging
git rm arquivo.txt

# Remove arquivo do Git mas mantém no sistema de arquivos
git rm --cached arquivo.txt
```

## Próximos Passos

No próximo módulo, aprenderemos sobre branches e merge, que permitem trabalhar em diferentes versões do seu código simultaneamente. 