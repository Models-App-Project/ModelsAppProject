# Convenção de commits

Nesse projeto, adotamos a **Convenção de Commits** para padronizar as mensagens de commit entre todas as equipes e garantir um histórico de versionamento limpo, claro e de fácil compreensão. Abaixo está a estrutura e as diretrizes seguidas para todos os commits.

## Estrutura de Commit

A mensagem de commit deve seguir a estrutura abaixo:

``` bash
<tipo>(<escopo>): <descrição>

<mensagem adicional/opcional>
```

### Componentes

1. **Tipo**: Define a categoria da alteração. É Obrigatório.
2. **Escopo**: Opcional. Indica a área ou módulo do projeto que foi alterado.
3. **Descrição**: Breve descrição do que foi alterado. Deve ser concisa, no imperativo e em minúsculas.
4. **Mensagem adicional**: Opcional. Explicação mais detalhada da mudança, caso nececssário.

## Tipos de Commit

- **feat**: Adição de uma nova funcionalidade.
  - Exemplo: ```feat(login): adicionar autenticação via OAuth```

- **fix**: Correção de bugs.
  - Exemplo: ```fix(profile): corrigir bug no carregamento da imagem de perfil```

- **refactor**: Alterações no código que não afetam a funcionalidade externa dos arquivos(ex: refatoração de código).
  - Exemplo: ```refactor(app): melhorar a organização dos arquivos```

- **chore**: Alterações menores ou ajustar no projeto que não afetam diretamente o código de produção.
  - Exemplo: ```chore(deps): atualizar dependências do projeto```

- **style**: Alterações puramente relacionadas ao estilo (ex: formatação, espaçamento, identação), sem alteração de lógica.
  - Exemplo: ```style(footer): corrigir espaçamento entre ícones.```

- **test**: Adição ou modificação de testes.
  - Exemplo: ```test(api): adicionar teste para o endpoint de usuários.```

- **docs**: Alterações na documentação.
  - Exemplo: ```docs(readme): atualizar instruções de instalação

- **perf**: Alterações que melhoram o desempenho.
  - Exemplo: ```perf(api): otimizar o processamento de requisições```

- **build**: Mudanças que afetam o sismte de build ou dependências externas.
  - Exemplo: ```build(docker): corrigir arquivo Dockerfile```

- **ci**: Mudanças em scripts e configurações de CI (integração contínua).
  - Exemplo: ```ci(jenkins): configurar pipeline no jenkins```

## Escopo

O escopo é opcional e pode ser usado para indicar qual parte do projeto foi afetada pela alteração (ex: *login*, *profile*, *api*, etc.).

### Exemplos de Commits

- ```feat(login): adicionar autenticação via OAuth```
- ```fix(profile): corrigir bug no carregamento da imagem de perfil```
- ```refactor(api): otimizar estrutura de rotas```
- ```chore(deps): atualizar dependências do projeto```
- ```dosc(readme): atualizar instruções de instalação```

## Mensagem Adicional (Opcional)

Se necessário, você pode adicionar uma descrição mais longa e detalhada sobre a mudança, logo após uma linha em branco. Esse campo é útil para explicar decisões importantes ou fornecer informações adicionais sobre a implementação.

``` bash
fix(profile): corrigir bug no carregamento da imagem de perfil

A correção envolve mudanças na lógica de renderização das imagens, garantindo que as imagens de perfil sejam carregadas corretamente em todas as situações de erro.
```

**Seguindo essa conveção, teremos um histórico de commits mais organizado, facilitando o trabalho em equipe e o processo de revisão de código.**
