# Arquitetura do Sistema: Models App Project

## 1. Visão Geral

O "Models App Project" é uma aplicação móvel desenvolvida em Flutter, com backend baseado em serviços Firebase. A arquitetura do sistema é orientada a serviços, utilizando Firebase para autenticação, armazenamento de dados e hosting de imagens.

## 2. Componentes Principais

### 2.1. Frontend (Flutter)

- **Linguagem:** Dart
- **Plataformas:** Android, iOS
- **Arquitetura:** MVVM (Model-View-ViewModel)
  - **Model:** Classes que representam os dados (ex: `User`, `Session`, `Photo`).
  - **View:** Telas e widgets do Flutter que exibem os dados.
  - **ViewModel:** Camada de lógica que interage com os serviços e atualiza as views.

### 2.2. Backend (Firebase)

- **Firebase Authentication:** Gerencia a autenticação de usuários.
- **Cloud Firestore:** Banco de dados NoSQL para armazenar dados do aplicativo, como sessões fotográficas, perfis de usuário e mensagens.
- **Firebase Storage:** Armazena imagens do portfólio e outras mídias.
- **Firebase Cloud Messaging (FCM):** Envia notificações push para os usuários.

## 3. Diagrama de Arquitetura

```plaintext
[Usuário]
   |
[Frontend (Flutter)]
   |
   +--> [Firebase Authentication] <---+
   |                                   |
   +--> [Cloud Firestore] <------------+---+ [Firebase Storage]
   |                                   |   |
   +--> [Firebase Cloud Messaging] <---+   |
```


## 4. Explicando a arquitetura MVVM (Model-view0ViewModel)

A arquitetura MVVM é um padrão de desig de software que separa a lógica de apresentação da lógica de negócios e dos dados. Ele é amplamente utlizado em aplicações que têm interfaces gráficas, como aplicativos móveis e web, e é especialmente popular em frameworks como WPF (Windows Presentation Foundation) e, mais recentemente, em frameworks como Flutter e SwiftUI.

### 4.1. Componentes do MVVVM

1. *Model*
   - **responsabilidade:** Representa a lógica de negócios e os dados da aplicação. O modelo é responsável por fornecer os dados que a ViewModel e a View vão consumir. Ele também pode encapsular regras de validação e lógica relacionada ao acesso a dados, seja por meio de APIs, banco de dados, ou outros serviços.

2. *View*
   - **Responsabilidade:** É a interface com o usuário, responsável por exibir os dados e capturar as interações do usuário. No MVVM, a View deve ser o mais "burra" possível, delegando a lógica de apresentação e manipulação de dados para a ViewModel.

3. *ViewModel*
   - **Responsabilidade:** Atua como um intermediário entre o Model e a View. A ViewModel mantém o estado da View, manipula a lógica de apresentação e comunica-se com o Model para buscar ou salvar dados. Ela também expõe propriedades e comando que a View pode vincular (binding). A ViewModel não deve conter referências à View, mantendo assim uma separação clara entre a lógica de apresentação e a interface do usuário.

### 4.2. Fluxo de Trabalho no MVVM

1. **Inicialização:** A aplicação inicializa a ViewModel, que, por sua vez, inicializa ou se conecta ao Model para buscar os dados necessários.

2. **Vinculação (Binding):** A View é ligada à ViewModel, tipicamente através de data binding, o que significa que os elementos da interface do usuário estão automaticamente sincronizados com as propriedades da ViewModel. Quando uma propriedade na ViewModel é alterada, a interface do usuário reflete essa mudança automaticamente e vice-versa.

3. **Interação do Usuário:** Quando o usuário interage com a View (por exemplo, ao clicar em um botão ou inserir texto em um campo), a ViewModel reage a essas interações através de comandos ou mudanças de propriedade.

4. **Atualização do Modelo:** A ViewModel pode, então, comunicar-se com o Model para atualizar os dados ou realizar ações como salvar as informações do usuário.

### 4.3. Benefícios do MVVM

- **Separação de Preocupações:** Mantém a lógica de negócios (Model), lógica de apresentação (ViewModel) e a interface do usuário (View) separadas, o que facilita a manutenção e a testabilidade do código.
- **Facilita o Teste Unitário:** Como a ViewModel não depende diretamente da View, ela pode ser facilmente testada sem precisar de um ambiente gráfico.
- **Reutilização de Código:** A lógica da ViewModel pode ser reutilizada em diferentes Views, e os Models podem ser reutilizados em diferentes ViewModels.
- **Manutenção:** Mudanças na UI não afetam a lógica de negócios, e vice-versa, facilitando a evolução do software.

### 4.4. MVVM em Flutter

No contexto do Flutter, o MVVM pode ser implementado com a ajuda de pacotes como *provider* ou *riverpod*, que facilitam o gerenciamento do estado e a separação de responsabilidades, mantendo a arquitetura da aplicação limpa e bem organizada.

Por exemplo, você pode ter uma View (um Widget do Flutter), uma ViewModel (uma classe Dart que estende *ChangeNotifier* ou usa *ValueNotifier*) e um Model que encapsula os dados. A ViewModel gerencia o estado da interface, e o Flutter pode ligar Widgets diretamente às propriedades da ViewModel usando os pacotes de gerenciamento de estado.

### 4.5. Por que escolhemos usar o MVVM?

Para o "Models App Project", o MVVM oferece uma abordagem robusta e escalável que facilita o desenvolvimento e a manutenção do aplicativo ao longo do semestre, proporcionando uma clara separação de responsabilidades, suporte a data binding, e maior testabilidade. Essas características tornam o MVVM uma escolha superior, especialmente para aplicativos móveis que requerem uma UI rica e dinâmica.
