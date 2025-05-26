# GitHub e Pull Requests

## Criando uma Conta no GitHub

1. Acesse [github.com](https://github.com)
2. Clique em "Sign up"
3. Siga as instruções para criar sua conta
4. Verifique seu email
5. Configure seu perfil

## Configurando o SSH

Para uma conexão segura com o GitHub:

```bash
# Gerar uma nova chave SSH
ssh-keygen -t ed25519 -C "seu.email@exemplo.com"

# Iniciar o ssh-agent
eval "$(ssh-agent -s)"

# Adicionar sua chave ao ssh-agent
ssh-add ~/.ssh/id_ed25519

# Copiar a chave pública
cat ~/.ssh/id_ed25519.pub
```

Adicione a chave pública nas configurações do GitHub:
1. Vá para Settings > SSH and GPG keys
2. Clique em "New SSH key"
3. Cole sua chave pública

## Criando um Repositório Remoto

1. No GitHub, clique em "New repository"
2. Dê um nome ao repositório
3. Adicione uma descrição
4. Escolha se será público ou privado
5. Inicialize com README (opcional)
6. Clique em "Create repository"

## Conectando um Repositório Local ao GitHub

```bash
# Adicionar o repositório remoto
git remote add origin git@github.com:usuario/repositorio.git

# Verificar os remotos
git remote -v

# Enviar o código para o GitHub
git push -u origin main
```

## Comandos de Sincronização

### git push

Envia commits locais para o repositório remoto:

```bash
# Enviar commits para a branch atual
git push

# Enviar para uma branch específica
git push origin nome-da-branch

# Forçar o push (use com cautela!)
git push -f origin nome-da-branch
```

### git pull

Atualiza seu repositório local com mudanças do remoto:

```bash
# Atualizar a branch atual
git pull

# Atualizar uma branch específica
git pull origin nome-da-branch
```

### git fetch

Baixa mudanças do remoto sem mesclá-las:

```bash
# Baixar todas as branches
git fetch

# Baixar uma branch específica
git fetch origin nome-da-branch
```

## Pull Requests

Pull Requests (PRs) são propostas de mudanças que você quer mesclar em um repositório.

### Criando um Pull Request

1. Faça push das suas mudanças para uma branch
2. No GitHub, vá para a página do repositório
3. Clique em "Pull requests"
4. Clique em "New pull request"
5. Selecione as branches base e de comparação
6. Adicione uma descrição detalhada
7. Clique em "Create pull request"

### Boas Práticas para Pull Requests

1. **Título Descritivo**
   - Seja claro e conciso
   - Use verbos no imperativo

2. **Descrição Detalhada**
   - O que foi feito
   - Por que foi feito
   - Como testar
   - Screenshots (se aplicável)

3. **Commits Organizados**
   - Commits atômicos
   - Mensagens claras
   - Sem commits de merge desnecessários

### Revisando Pull Requests

1. **Verificação de Código**
   - Revisar as mudanças
   - Verificar a qualidade do código
   - Testar as funcionalidades

2. **Comentários**
   - Seja construtivo
   - Explique suas sugestões
   - Reconheça o bom trabalho

3. **Aprovação**
   - Aprove apenas quando estiver satisfeito
   - Peça mudanças se necessário
   - Use os emojis do GitHub para feedback

## GitHub Flow

1. **Criar uma Branch**
   ```bash
   git checkout -b feature-nova
   ```

2. **Fazer Commits**
   ```bash
   git add .
   git commit -m "Adiciona nova funcionalidade"
   ```

3. **Push para GitHub**
   ```bash
   git push origin feature-nova
   ```

4. **Criar Pull Request**
   - No GitHub, crie um PR
   - Aguarde revisão
   - Faça ajustes se necessário

5. **Merge**
   - Após aprovação, faça o merge
   - Delete a branch

## Recursos Adicionais do GitHub

### Issues

- Rastrear bugs
- Sugerir melhorias
- Gerenciar tarefas

### Projects

- Organizar trabalho
- Visualizar progresso
- Gerenciar sprints

### Actions

- Automatizar workflows
- CI/CD
- Testes automatizados

## Dicas para Colaboração

1. **Comunicação**
   - Use issues para discussão
   - Mantenha PRs atualizados
   - Responda a comentários

2. **Documentação**
   - Mantenha o README atualizado
   - Documente mudanças importantes
   - Use comentários no código

3. **Código Limpo**
   - Siga padrões de código
   - Mantenha o código testável
   - Evite código duplicado

## Conclusão

GitHub e Pull Requests são ferramentas essenciais para colaboração em projetos de software. Dominar esses conceitos é fundamental para trabalhar em equipe e contribuir para projetos open source.

**Lembre-se:** A prática leva à perfeição no uso do Git e GitHub! 