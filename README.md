# Sistema de Estacionamento

Aplicação de console desenvolvida em **C# e .NET** para simular o gerenciamento de um estacionamento.

O sistema permite cadastrar veículos, remover veículos, calcular o valor da permanência e listar as placas atualmente estacionadas.

---

## Objetivos de aprendizado

O projeto foi desenvolvido para praticar:

* Fundamentos da linguagem C#;
* Variáveis e tipos de dados;
* Classes e objetos;
* Métodos;
* Construtores;
* Encapsulamento;
* Listas;
* Estruturas condicionais;
* Estruturas de repetição;
* Entrada e saída de dados;
* Operações com valores monetários;
* Menus interativos;
* Validação de dados;
* Aplicações de console.

---

## Funcionalidades

O sistema oferece um menu com as seguintes opções:

```text
1. Cadastrar veículo
2. Remover veículo
3. Listar veículos
4. Encerrar
```

### Cadastrar veículo

Solicita a placa do veículo e adiciona o registro à lista de veículos estacionados.

### Remover veículo

Solicita a placa e a quantidade de horas de permanência.

Caso a placa exista, o sistema:

1. Calcula o valor;
2. Remove o veículo;
3. Exibe o total a pagar.

### Listar veículos

Exibe todas as placas presentes no estacionamento.

Caso a lista esteja vazia, informa que não existem veículos estacionados.

### Encerrar

Finaliza a execução da aplicação.

---

## Regra de cobrança

A cobrança utiliza:

* Um preço inicial;
* Um preço adicional por hora;
* A quantidade de horas estacionadas.

A fórmula utilizada é:

```text
Valor total = preço inicial + (preço por hora × horas)
```

Exemplo:

```text
Preço inicial: R$ 5,00
Preço por hora: R$ 2,00
Permanência: 3 horas

Total = 5 + (2 × 3)
Total = R$ 11,00
```

---

## Classe Estacionamento

A classe central do projeto possui:

```text
precoInicial
precoPorHora
veiculos
```

### precoInicial

Valor fixo cobrado pela entrada do veículo.

### precoPorHora

Valor cobrado por cada hora de permanência.

### veiculos

Lista de strings que armazena as placas dos veículos.

---

## Métodos principais

### AdicionarVeiculo

Recebe uma placa e adiciona o veículo à lista.

```csharp
public void AdicionarVeiculo()
{
    Console.WriteLine("Digite a placa do veículo:");
    string placa = Console.ReadLine();

    veiculos.Add(placa);
}
```

### RemoverVeiculo

Verifica se o veículo está estacionado, solicita a quantidade de horas e calcula o valor.

### ListarVeiculos

Percorre a lista e apresenta todas as placas cadastradas.

---

## Fluxo da aplicação

```text
Início
  ↓
Configuração dos preços
  ↓
Exibição do menu
  ↓
Escolha da operação
  ├── Cadastrar
  ├── Remover
  ├── Listar
  └── Encerrar
```

O menu permanece ativo até que o usuário escolha a opção de encerramento.

---

## Arquitetura do projeto

```text
SistemaEstacionamento/
├── DesafioFundamentos/
│   ├── Models/
│   │   └── Estacionamento.cs
│   ├── Program.cs
│   └── DesafioFundamentos.csproj
├── diagrama_classe_estacionamento.png
└── README.md
```

---

## Tecnologias utilizadas

* C#;
* .NET;
* Aplicação de console;
* Programação orientada a objetos;
* Git e GitHub.

---

## Conceitos aplicados

### Lista

A estrutura `List<string>` armazena as placas dos veículos.

```csharp
List<string> veiculos = new();
```

### Estrutura condicional

O sistema verifica se a placa está cadastrada antes de remover o veículo.

### Estrutura de repetição

O menu é apresentado repetidamente enquanto a aplicação estiver em execução.

### Métodos

Cada funcionalidade foi separada em um método específico.

### Valores decimais

O tipo `decimal` é utilizado para representar valores monetários.

---

## Exemplo de utilização

```text
Digite o preço inicial:
5

Digite o preço por hora:
2

1 - Cadastrar veículo
2 - Remover veículo
3 - Listar veículos
4 - Encerrar

Opção: 1

Digite a placa:
ABC1D23

Veículo cadastrado com sucesso.
```

Ao remover:

```text
Digite a placa:
ABC1D23

Digite a quantidade de horas:
3

O veículo ABC1D23 foi removido.
Total a pagar: R$ 11,00
```

---

## Destaques técnicos

### Separação das operações

Cada ação do estacionamento possui seu próprio método:

```text
AdicionarVeiculo()
RemoverVeiculo()
ListarVeiculos()
```

### Menu interativo

O `Program.cs` controla o fluxo da aplicação e chama os métodos conforme a opção selecionada.

### Controle em memória

Os veículos permanecem armazenados em uma lista durante a execução do programa.

### Cálculo monetário

O uso de `decimal` evita problemas comuns de precisão encontrados em tipos de ponto flutuante.

---

## Como executar o projeto

### Pré-requisitos

* .NET SDK;
* Git;
* Visual Studio, Visual Studio Code ou Rider.

### 1. Clone o repositório

```bash
git clone https://github.com/enricobarni/SistemaEstacionamento.git
```

### 2. Acesse a pasta do projeto

```bash
cd SistemaEstacionamento/DesafioFundamentos
```

### 3. Restaure as dependências

```bash
dotnet restore
```

### 4. Execute o programa

```bash
dotnet run
```

---

## Aprendizados obtidos

Durante o desenvolvimento, foram praticados:

* Sintaxe básica do C#;
* Classes;
* Construtores;
* Métodos;
* Listas;
* Condicionais;
* Laços de repetição;
* Entrada de dados;
* Formatação monetária;
* Menus de console;
* Validação de registros;
* Organização de projetos .NET.

---

## Autor

Desenvolvido por **Enrico Barni Venturato**.

* GitHub: [enricobarni](https://github.com/enricobarni)
* LinkedIn: [Enrico Barni Venturato](https://www.linkedin.com/in/enrico-barni-venturato/)

---

Este projeto faz parte da minha jornada de aprendizado em fundamentos do C#, .NET e programação orientada a objetos.
