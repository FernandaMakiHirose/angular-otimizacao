# Conceitos avançados de performance e otimização usando Angular
## Pré-requisitos
- Angular
- Java
- IDE

# Comandos
Após clonar o projeto:
>npm install
 
Abra o `localhost:4200` no seu navegador:
>npm start

## enableProdMode
É uma parte do Angular que adiciona outras configurações, remove debuggers que não precisa, otimiza o código para produção e também remove códigos da árvore de desenvolvimento do Angular que são focadas somente em desenvolvimento. 

![enableprodmode](https://user-images.githubusercontent.com/72028645/130243418-ee9cfba6-af2d-48cb-91f7-53fd57649ba5.png)

## Carregamento tardio de recursos
É uma forma de construir os módulos, de forma que eles fiquem em bundles diferentes. <br>
1- Configurar a rota, fazer o lazy load do bundle, quando clicar em um link `about` vai importar o arquivo e depois o módulo. <br>
3- Adiciona o path do `about` no `app-routing.module.ts`, adiciona o loadChildren, passa o arquivo, faz o then e retorna o m.AboutModule 

![bundle](https://user-images.githubusercontent.com/72028645/130244453-30a5d3ff-79fa-45da-bab3-8fb7a84b0bc0.png)

2- O `about-routing.module.ts` perde o path

![Screenshot_1](https://user-images.githubusercontent.com/72028645/130245048-3a0a8ed9-7de4-463e-b511-5d52c13a1c3c.png)

4- Remover o `AboutModule` do imports do `app.module.ts`

## preloadingStrategy 
É fazer o preloading dos dados para já serem carregados em vez de serem carregados quando executar uma ação.

![Screenshot_2](https://user-images.githubusercontent.com/72028645/130246665-fb397f27-3154-4e36-ae58-9a229923601b.png)

## changeDetection
O `.onPush` torna o componente imutável, ele só vai tirar uma nova versão do componente se o @Input() for alterado

![Screenshot_3](https://user-images.githubusercontent.com/72028645/130248171-696e420a-923c-4ebf-97b1-873b17984590.png)


### Bibliotecas

- [Angular](https://angular.io)
- [Bootstrap 4](https://getbootstrap.com)
- [Font Awesome](http://fontawesome.io)
- [RxJS](http://reactivex.io/rxjs)
- [ng-bootstrap](https://ng-bootstrap.github.io)
- [ngx-translate](https://github.com/ngx-translate/core)
- [Lodash](https://lodash.com)

#### Guias

- [Angular](docs/coding-guides/angular.md)
- [TypeScript](docs/coding-guides/typescript.md)
- [Sass](docs/coding-guides/sass.md)
- [HTML](docs/coding-guides/html.md)
- [Unit tests](docs/coding-guides/unit-tests.md)
- [End-to-end tests](docs/coding-guides/e2e-tests.md)

#### Documentação

- [I18n guide](docs/i18n.md)
- [Working behind a corporate proxy](docs/corporate-proxy.md)
- [Updating dependencies and tools](docs/updating.md)
- [Using a backend proxy for development](docs/backend-proxy.md)
- [Browser routing](docs/routing.md)
