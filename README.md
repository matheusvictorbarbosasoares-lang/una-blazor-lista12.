#  EcoMonitor - Lista 12 (Blazor)

##  Identificação

**Nome:** Matheus Victor Barbosa Soares
**Curso:** Ciência da Computação  / UNA 1º semestre

---

##  Sobre o Projeto

O **EcoMonitor** é uma aplicação desenvolvida em Blazor que simula um sistema de gamificação para incentivar ações sustentáveis.

O usuário pode registrar ações como:

* Reciclagem de plástico
* Plantio de árvores
* Descarte de eletrônicos

Cada ação soma pontos e atualiza o progresso em tempo real.

---

##  Heurísticas de Nielsen Aplicadas

### 1. Visibilidade do Status do Sistema

O sistema mostra o total de pontos em tempo real sempre que o usuário clica no botão, permitindo que ele acompanhe seu progresso imediatamente.

### 2. Feedback Imediato

Ao clicar no botão "Adicionar", o sistema responde instantaneamente:

* Atualizando o contador
* Preenchendo a barra de progresso
* Exibindo uma mensagem de conquista ao atingir 100 pontos

---

##  Guia de Execução

### Pré-requisitos:

* .NET instalado

### Passos:

```bash
dotnet build
dotnet run --launch-profile https
```

Depois, abra o navegador em:

```
https://localhost:xxxx
```

---

##  Explicação Técnica

O componente `EcoStatus.razor` foi desenvolvido de forma reutilizável utilizando o atributo `[Parameter]`.

Exemplo:

```csharp
[Parameter]
public int Peso { get; set; }
```

O `[Parameter]` permite que diferentes valores sejam passados para o componente, possibilitando reutilizar o mesmo componente para diferentes ações.

Na `Home.razor`, o componente é utilizado várias vezes com valores diferentes:

```razor
<EcoStatus Titulo="Reciclagem de Plástico" Peso="1" />
<EcoStatus Titulo="Plantio de Árvores" Peso="10" />
<EcoStatus Titulo="Descarte de Eletrônicos" Peso="5" />
```

Isso evita repetição de código e torna o sistema mais organizado e escalável.

---

##  Funcionalidades Extras

* Barra de progresso dinâmica
* Mudança de cor ao atingir meta
* Mensagem de conquista ao alcançar 100 pontos

---

##  Conclusão

O projeto demonstra na prática conceitos importantes de:

* Componentização
* Reutilização de código
* Manipulação de estado no Blazor
* Princípios de UX

---
