# Branches e Merge

## O que são Branches?

Branches (ramificações) são linhas independentes de desenvolvimento que permitem trabalhar em diferentes versões do seu código simultaneamente. Pense nelas como cópias do seu código que podem evoluir independentemente.

## Por que Usar Branches?

1. **Desenvolvimento Paralelo**: Trabalhar em múltiplas funcionalidades ao mesmo tempo
2. **Isolamento**: Testar mudanças sem afetar o código principal
3. **Colaboração**: Diferentes desenvolvedores podem trabalhar em branches separadas
4. **Organização**: Manter o código principal estável enquanto desenvolve novas features

## Comandos Básicos de Branches

### Listar Branches

```bash
# Listar branches locais
git branch

# Listar todas as branches (incluindo remotas)
git branch -a
```

### Criar uma Nova Branch

```bash
# Criar uma nova branch
git branch nova-feature

# Criar e mudar para a nova branch
git checkout -b nova-feature
```

### Mudar de Branch

```bash
# Mudar para uma branch existente
git checkout nome-da-branch

# No Git mais recente, você também pode usar
git switch nome-da-branch
```

### Deletar uma Branch

```bash
# Deletar uma branch local
git branch -d nome-da-branch

# Forçar a deleção de uma branch
git branch -D nome-da-branch
```

## Trabalhando com Branches

### Exemplo Prático

```bash
# 1. Criar uma nova branch para uma feature
git checkout -b feature-login

# 2. Fazer algumas alterações
echo "Nova funcionalidade de login" > login.txt

# 3. Adicionar e commitar as mudanças
git add login.txt
git commit -m "Adiciona funcionalidade de login"

# 4. Voltar para a branch principal
git checkout main

# 5. Verificar que o arquivo não existe na main
ls
```

## Merge

Merge é o processo de combinar mudanças de uma branch em outra.

### Tipos de Merge

1. **Fast-forward**: Quando não há commits na branch de destino
2. **Three-way merge**: Quando há commits em ambas as branches

### Realizando um Merge

```bash
# 1. Mudar para a branch de destino
git checkout main

# 2. Realizar o merge
git merge feature-login
```

### Resolvendo Conflitos

Quando o Git não consegue resolver automaticamente as diferenças, você precisa resolver manualmente:

1. O Git marca os arquivos com conflitos
2. Edite os arquivos para resolver os conflitos
3. Adicione os arquivos resolvidos
4. Complete o merge

Exemplo de conflito:
```
<<<<<<< HEAD
Linha na branch atual
=======
Linha na branch que está sendo mergeada
>>>>>>> feature-login
```

## Boas Práticas

1. **Nomes Descritivos**
   - Use nomes que descrevam o propósito da branch
   - Exemplos: `feature-login`, `bugfix-header`, `hotfix-security`

2. **Branches Curtas**
   - Mantenha as branches atualizadas com a main
   - Faça merges frequentes para evitar conflitos complexos

3. **Commits Limpos**
   - Mantenha commits organizados e bem documentados
   - Facilita a resolução de conflitos

## Comandos Avançados

### git merge --abort

Cancela um merge em andamento:
```bash
git merge --abort
```

### git branch --merged

Lista branches que já foram mergeadas:
```bash
git branch --merged
```

### git branch --no-merged

Lista branches que ainda não foram mergeadas:
```bash
git branch --no-merged
```

## Estratégias de Branching

### Git Flow

1. `main`: Código em produção
2. `develop`: Código em desenvolvimento
3. `feature/*`: Novas funcionalidades
4. `release/*`: Preparação para release
5. `hotfix/*`: Correções urgentes

### GitHub Flow

1. `main`: Sempre deployável
2. Branches de feature para cada mudança
3. Pull requests para revisão
4. Merge após aprovação

## Próximos Passos

No próximo módulo, aprenderemos sobre GitHub e Pull Requests, que são essenciais para colaboração em equipe. 