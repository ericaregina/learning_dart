# Dart: Conceitos e Exemplos de Código

Dart é uma linguagem de programação desenvolvida pela Google, bastante utilizada para o desenvolvimento de aplicativos multiplataforma, especialmente em conjunto com o framework Flutter. É conhecida por sua **sintaxe simples**, **desempenho otimizado** e uma **biblioteca padrão robusta**, que oferece diversas funcionalidades essenciais para o desenvolvimento de software moderno.

## 1. Tipagem em Dart

Dart possui tipagem estática e forte, o que significa que cada variável deve ser associada a um tipo específico que não muda durante a execução. Porém, ela também possui tipagem adaptativa, permitindo o uso de `var` e `dynamic`. Com `var`, o tipo é inferido automaticamente pelo valor atribuído. Com `dynamic`, a variável pode assumir diferentes tipos em tempo de execução, tornando Dart flexível em variados contextos.

```dart
void main() {
  // Tipagem forte
  int idade = 25;
  String nome = "Érica";

  // Tipagem adaptativa com 'var'
  var cidade = "Porto Alegre"; // Infere automaticamente como String

  // Tipagem adaptativa com 'dynamic'
  dynamic valor = 10;
  valor = "Pode ser qualquer tipo"; // Mudando o tipo em tempo de execução

  print("Nome: $nome, Idade: $idade, Cidade: $cidade, Valor: $valor");
}
```

## 2. Controle de Fluxo

Dart inclui estruturas de controle de fluxo como  `if, else, for, while, switch e do-while `, fundamentais para controlar a lógica do programa com base em condições e iterações. O uso de operadores matemáticos em Dart facilita cálculos diretos e é essencial para muitas operações.

```dart
Copiar código
void main() {
  // if-else
  int numero = 10;
  if (numero > 5) {
    print("Número é maior que 5");
  } else {
    print("Número é 5 ou menor");
  }

  // switch-case
  String diaSemana = "terça";
  switch (diaSemana) {
    case "segunda":
      print("Hoje é segunda-feira");
      break;
    case "terça":
      print("Hoje é terça-feira");
      break;
    default:
      print("Outro dia");
  }

  // for-loop
  for (int i = 0; i < 3; i++) {
    print("Contando: $i");
  }
}
```
## 1. Tipagem em Dart

Dart facilita operações matemáticas básicas, que são frequentemente usadas no desenvolvimento de software. Abaixo estão exemplos de operações de soma, subtração, multiplicação e divisão.

```dart
Copiar código
void main() {
  int a = 10;
  int b = 5;

  int soma = a + b;
  int subtracao = a - b;
  int multiplicacao = a * b;
  double divisao = a / b;

  print("Soma: $soma, Subtração: $subtracao, Multiplicação: $multiplicacao, Divisão: $divisao");
}
```
## 3. Operadores Matemáticos
Dart facilita operações matemáticas básicas, que são frequentemente usadas no desenvolvimento de software. Abaixo estão exemplos de operações de soma, subtração, multiplicação e divisão.

```dart
Copiar código
void main() {
  int a = 10;
  int b = 5;

  int soma = a + b;
  int subtracao = a - b;
  int multiplicacao = a * b;
  double divisao = a / b;

  print("Soma: $soma, Subtração: $subtracao, Multiplicação: $multiplicacao, Divisão: $divisao");
}
```

## 4. Classes, Herança, Métodos, @override, super e static
Dart é uma linguagem orientada a objetos e utiliza conceitos como classes e herança para organizar e reutilizar código. Abaixo, o operador  `extends` permite que uma classe herde propriedades e métodos de outra,  `@override` e  `super` ajudam na personalização e acesso a métodos da superclasse, e  `static` permite o acesso a membros de classe sem necessidade de instância.

```dart
Copiar código
class Animal {
  String nome;

  Animal(this.nome);

  void som() {
    print("$nome faz um som.");
  }
}

class Cachorro extends Animal {
  // Construtor da subclasse
  Cachorro(String nome) : super(nome);

  // Sobrescrevendo o método
  @override
  void som() {
    super.som(); // Chamando o método da superclasse
    print("$nome faz: Au au!");
  }

  // Método estático
  static void informacao() {
    print("Os cachorros são animais domésticos.");
  }
}

void main() {
  var meuCachorro = Cachorro("Rex");
  meuCachorro.som();

  // Chamando o método estático
  Cachorro.informacao();
}
```

## 5. Listas
As listas em Dart são usadas para armazenar coleções ordenadas de itens e oferecem métodos para manipulação de dados, como adicionar, remover e filtrar elementos. Abaixo estão exemplos de uso básico com adição, remoção e iteração sobre os elementos.

```dart
Copiar código
void main() {
  List<String> frutas = ["Maçã", "Banana", "Laranja"];

  // Adicionando elementos
  frutas.add("Manga");

  // Removendo um elemento
  frutas.remove("Banana");

  // Acessando elementos
  print("Primeira fruta: ${frutas[0]}");

  // Iterando sobre a lista
  for (var fruta in frutas) {
    print("Fruta: $fruta");
  }
}
```
