# Desafio App Moobie

Este repositório contém as diretrizes para o desafio de programação do App Moobie. Ele é válido tanto para iOS quanto Android porém só é esperado que você faça uma plataforma usando código nativo.

# Requisitos
Crie um aplicativo que permita que o usuário escolha a marca, modelo e ano de seu carro, para obter esas informação você deve utilizar a API da FIPE fornecida por nós. Na Moobie focamos muito em garantir a melhor experiência possível para o usuário, sinta-se livre para fazer a UI como achar melhor. É esperado que seu App siga as Human Interface Guidelines/User Interface Guidelines.

Você tem duas opções de como fazer seu app e essa escolha depende do seu conhecimento, lembrando que encorajamos que você aprenda algo novo com esse teste!

## App sem persistência
O app abre na tela de escolha de modelo e após essa escolha aparece uma tela com os detalhes selecionados e o preço do veículo de acordo com a tabela FIPE.

## App com peristência
O app abre com uma lista de carros salvos, há a opção de ver detalhes do carro (mesma tela que a opção sem persistência, você pode supor que estes valores não mudarão nunca) e após adicionar um carro o usuário retorna para a lista, que agora contém o novo carro adicionado.

## iOS
* É esperado que o projeto compile sem erros / warnings na versão atual do Xcode na App Store.
* O projeto deve ser escrito em Swift 3.
* O projeto deve suportar iOS 9 e será testado na versão mais recente do iOS.
* É permitido o uso de bibliotecas externas, assim como gerenciadores de dependências. Elas podem ser escritas em qualquer linguagem.
* As telas devem ser feitas com Auto Layout e não podem apresentar logs de erro no console.
* Provavelmente faremos perguntas sobre o seu código, não saia colando tudo do Stack Overflow :)

## Android
* É esperado que o projeto compile sem erros / warnings na versão atual do Android Studio.
* O projeto deve ser escrito em Java e/ou Kotlin.
* O projeto deve ter Base SDK 16 e será testado na versão mais recente do Android.
* É permitido o uso de bibliotecas externas, assim como gerenciadores de dependências.
* Provavelmente faremos perguntas sobre o seu código, não saia colando tudo do Stack Overflow :)

# Extras

* Tratamento de cenários de erro (falta de conexão com a internet, indisponibilidade do servidor, etc)
* Pull to refresh
* Testes Unitários
* Testes de UI
* 100% de Cobertura de código
* Uso de Rx/ReactiveCocoa
* DI
* L10n
* A11y

# iOS
* Layout por código
* Uso de SwiftLint
* Dynamic Type
* App universal

# Especificação da API
Todas os endpoints abaixo são relativos a http://fipe-api.herokuapp.com

## `GET /cars/brand`
Retorna uma lista de marcas
```javascript
[{"marca":"Acura"},{"marca":"Agrale"},{"marca":"Alfa Romeo"},{"marca":"AM Gen"},{"marca":"Asia Motors"},{"marca":"ASTON MARTIN"},{"marca":"Audi"}]
```

## `GET /cars/brand/:brand`
Retorna modelos de uma marca específica
```javascript
[{"codigo_fipe":"038003-2","modelo":"Integra GS 1.8","ano":"1992"},{"codigo_fipe":"038003-2","modelo":"Integra GS 1.8","ano":"1991"}]
```

## `GET /cars/:fipe_code/:year`
Retorna os dados sobre um modelo/ano específico
```javascript
[{"codigo_fipe":"038002-4","marca":"Acura","modelo":"Legend 3.2/3.5","ano":"1992","valor":16678}]
```

# Prazo
Esperamos que você faça tudo em até duas semanas, se você não conseguir fazer tudo nos envie mesmo assim e se tiver algum problema fale conosco, estamos aqui para ajudar ;)

# Submissão

Você tem duas opções:  

1) Você pode fazer um _pull request_ no nosso [repositório __público__](https://github.com/Moobie/desafio-mobile). Note que seu *fork* ficará público para qualquer pessoa ver.

2) Caso você prefira um pouco de privacidade, crie um repositório com o nome **desafio-mobile** na sua conta do GitHub, Bitbucket ou GitLab, inclua os usuários abaixo como colaboradores (acesso de leitura) e nos envie um email avisando.

| Plataforma | Email | Usuário |
| -- | -- | -- |
| iOS | francesco@moobie.com.br | fpg1503 |
| Android | danilo@moobie.com.br | danmalafaia |
| Android | hp@moobie.com.br | eduardolal86  |
