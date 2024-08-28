# Guia de Contribuição

Obrigado por contribuir com o **Models App Project**! Este guia irá ajudá-lo a entender como enviar um Pull Request (PR) de forma eficiente e organizada.

## Passos para Contribuir

1. **Fork do Repositório**
   - Faça um fork deste repositório para sua conta pessoal do GitHub.

2. **Clone o Repositório Forked**
   - Clone o repositório forked para sua máquina local:
  
     ```bash
     git clone https://github.com/seu-usuario/models-app-project.git
     cd models-app-project
     ```

3. **Crie uma Branch para a Sua Feature/Bugfix**
   - Utilize uma nomenclatura clara para a sua branch, como `feature/nome-da-feature` ou `bugfix/nome-do-bug`:

     ```bash
     git checkout -b feature/nome-da-feature
     ```

4. **Implemente a Sua Feature ou Corrija o Bug**
   - Certifique-se de seguir as diretrizes de código e manter o padrão arquitetural MVVM.
   - Teste sua implementação localmente para garantir que tudo está funcionando conforme esperado.

5. **Escreva Testes**
   - Adicione testes unitários e de integração para sua feature ou bugfix, se aplicável.
   - Certifique-se de que todos os testes existentes ainda estão passando:
  
     ```bash
     flutter test
     ```

6. **Faça Commit das Suas Alterações**
   - Utilize mensagens de commit claras e significativas:

     ```bash
     git add .
     git commit -m "Implementa [feature/bugfix]: descrição detalhada"
     ```

7. **Faça Push para o Seu Repositório Forked**
   - Envie suas alterações para o repositório forked:

     ```bash
     git push origin feature/nome-da-feature
     ```

8. **Abra um Pull Request**
   - Vá até o repositório original do "Models App Project" e clique em "Compare & pull request".
   - Preencha o formulário do PR com as seguintes informações:
     - **Título**: Resumido e descritivo.
     - **Descrição**: Detalhe a motivação para a mudança, quais problemas foram resolvidos, como a implementação foi feita e como testá-la.
     - **Issue Relacionada**: Se aplicável, link para a issue relacionada.

9. **Aguarde Revisão**
   - O PR será revisado por um dos responsáveis pelo projeto. Seja receptivo aos comentários e pronto para fazer ajustes, se necessário.
   - Lembre-se de que seu PR pode ser aprovado, solicitado para mudanças, ou rejeitado com explicação.

10. **Incorpore Feedback e Faça Novos Commits**
    - Se solicitado, faça as mudanças necessárias e adicione novos commits à sua branch.
    - Não crie um novo PR; adicione os commits ao PR existente.

11. **PR Aprovado**
    - Após a aprovação, um dos mantenedores fará o merge do PR.
    - Você pode deletar a branch local e remota após o merge:

      ```bash
      git checkout main
      git pull origin main
      git branch -d feature/nome-da-feature
      git push origin --delete feature/nome-da-feature
      ```

## Diretrizes de Código

- **Consistência com a Arquitetura MVVM**: Mantenha a separação de responsabilidades entre Model, ViewModel e View.
- **Padrões de Código**: Siga as convenções de código utilizadas no projeto. Utilize um linter para manter a qualidade do código.
- **Documentação**: Documente suas funções, classes e métodos conforme necessário para garantir que outros desenvolvedores possam entender sua contribuição.
- **Commit Messages**: Utilize mensagens de commit descritivas e no tempo presente. Exemplo: `"Adiciona funcionalidade de login"`.

## Estrutura do Pull Request

- **Título**: Resumido e claro.
- **Descrição**:
  - **Motivação**: Por que essa mudança é necessária?
  - **Implementação**: Como a feature foi implementada?
  - **Testes**: Como os testes foram realizados? Quais foram os cenários testados?
- **Checklist**:
  - [ ] Minha implementação segue os padrões estabelecidos.
  - [ ] Adicionei testes adequados para esta mudança.
  - [ ] Verifiquei se a mudança não quebra funcionalidades existentes.

## Revisão de Código

- Feedback será fornecido no PR. Respeite os comentários e esteja disposto a fazer ajustes.
- Discussões devem ser civilizadas e focadas em melhorar o código.

## Comunicação

- Utilize a seção de comentários no PR para discutir mudanças e solicitar clarificações.
- Para discussões mais amplas, utilize os canais de comunicação estabelecidos pelo time.

## Agradecimentos

Sua contribuição é extremamente valiosa para o sucesso deste projeto! Obrigado por se juntar a nós e por seu empenho em melhorar o "Models App Project".

---

Caso tenha dúvidas sobre o processo, sinta-se à vontade para perguntar! Estamos aqui para ajudar.
