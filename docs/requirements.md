# Requisitos do Projeto: Models App Project

## 1. Visão geral

O "Models App Project" é um aplicativo desenvolvido para facilitar a gestão de sessões fotográficas por uma fotógrafa, permitindo também que modelos acompanhem e interajam com as sessões e com o portfólio.

## 2. Requisitos Funcionais

### 2.1. Login dos Administradores
  
- Os administradores devem ser capazes de criarem uma conta usando e-mail e senha.
- O Sistema deve suportar autenticação via '?Firebase Authentication?'
- Os administradores devem poder redefinir suas senhas através da WebPage.

### 2.2. Dashboard

- Após o login, os administradores devem ser direcionados ao dashboard da aplicação com as seguinte opções:
  - Ver estado atual da aplicação
  - Gerenciar Modelos
  - Verificar dados e portfólios
  - Configurações

### 2.3. Gerenciamento de Sessões

- A fotógrafa deve poder criar, editar e excluir sessões fotográficas.
- As modelos devem receber notificações sobre novas sessões ou alterações em sessões existentes.
- O sistema deve permitir que a fotógrafa envie lembretes para as modelos.

### 2.4. Portfólio

- A fotógrafa e as modelos devem poder visualizar e organizar fotos no portfólio.
- O sistema deve suportar o upload de imagens em formatos comuns (ex: JPG, PNG).
- As fotos devem ser categorizadas por sessões ou álbuns.

### 2.5. Configurações

- As modelos devem poder editar seu perfil, incluindo informações pessoais e preferências.
- O sistema deve permitir que o usuário configure notificações.

## 3. Requisitos Não Funcionais

### 3.1. Desempenho

- O aplicativo deve carregar as telas principais em menos de 2 segundos na maioria dos dispositivos.
- O sistema deve suportar até 100 usuários simultâneos sem degradação significativa de desempenho.

### 3.2. Segurança

- Todas as comunicações devem ser criptografadas (HTTPS).
- Senhas devem ser armazenadas de forma segura, utilizando hashing e salting.

### 3.3. Compatibilidade

- O aplicativo deve ser compatível com Android (versão mínima: 8.0) e iOS (versão mínima: 12.0).
- O sistema deve funcionar corretamente em dispositivos com diferentes resoluções de tela.

### 3.4. Usabilidade

- O design deve ser intuitivo, permitindo fácil navegação entre as funcionalidades.
- Deve haver tutoriais ou dicas para ajudar novos usuários a se familiarizarem com o aplicativo.

## 4. Restrições

- O projeto deve ser concluído até o final do semestre.
- O aplicativo deve ser desenvolvido usando Flutter para suportar Android e iOS.
