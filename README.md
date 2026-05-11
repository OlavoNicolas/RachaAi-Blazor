# RachaAí - Dashboard Financeiro com Blazor

Projeto desenvolvido em C# utilizando ASP.NET Core Blazor e Bootstrap para a disciplina de Interação Humano Computador e UX.

## Objetivo

Construir uma interface de Dashboard Financeiro para o aplicativo fictício “RachaAí”, aplicando conceitos de:

* Hierarquia visual
* Componentização
* Responsividade
* UX/UI
* Reutilização de componentes

## Estrutura do Projeto

```text
Models/
    Grupo.cs

Pages/
    Dashboard.razor

Shared/
    GrupoCard.razor
```

## Funcionalidades Implementadas

### Dashboard Principal

A página principal exibe:

* Cards de resumo financeiro
* Lista dinâmica de grupos
* Botão de ação rápida (FAB)

### Componentização

Foi criado o componente reutilizável:

```text
GrupoCard.razor
```

Responsável por renderizar:

* Nome do grupo
* Categoria
* Valor pendente
* Status financeiro

### Modelagem de Dados

Foi criada a classe:

```csharp
Grupo
```

com os atributos:

* Nome
* Categoria
* ValorPendente
* NoVermelho

### Responsividade

Foi utilizado o sistema de Grid do Bootstrap:

* row
* col-md
* col-lg

permitindo adaptação em diferentes tamanhos de tela.

### UX e Hierarquia Visual

Foram aplicados:

* Cards Bootstrap
* Cores semânticas (`text-danger` e `text-success`)
* Destaque visual para saldo
* Organização por prioridade de informação

### Tratamento de Dados Vazios

A aplicação exibe mensagem amigável caso não existam grupos cadastrados.

## Implementação Blazor

A hierarquia visual planejada no wireframe foi transformada em componentes reutilizáveis utilizando Razor Components do Blazor.

A página `Dashboard.razor` é responsável pelo gerenciamento e renderização dos dados, enquanto `GrupoCard.razor` encapsula a interface de cada grupo financeiro.

Foi utilizado:

* `@foreach`
* `[Parameter]`
* `@if`
* Data Binding
* Componentes reutilizáveis

## Dificuldade Técnica

O principal desafio foi compreender a comunicação entre componentes no Blazor, especialmente o uso de parâmetros (`[Parameter]`) para envio de dados do Dashboard para o componente `GrupoCard`.

Também houve dificuldade inicial na compreensão da mistura entre HTML, Bootstrap e código C# dentro dos arquivos `.razor`.
