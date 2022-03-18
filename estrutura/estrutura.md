## Data Types (Tipos de dados)

#### Variable Declaration and Assignment (Declaração e atribuição de variável)
```dart
void main() {
  TIPO NOME = VALOR;

  bool b = 2 != 4 || 7 == 7; // true

  int i = 4 + 10 * 5; // 54

  double d = 3 - 10 / 4; // 0.5

  num n = 4 + 7 / 8; // 4.875

  String s = 'texto ${2 + 3}' + ' concatecado'; // 'texto 5 concatecado'

  // Dart assim como C# suporta inferência de tipo, deduzindo o tipo da variável a partir do valor atribuído a ela
  var a = 5; // a é inferido como int
  var c = false; // c é inferido como bool

  // também suporta variáveis dinâmicas qe aceitam qualqer tipo de valor, incluindo null e podem ser reatribuídas para outros tipos de valores. Object também pode ser usado
  dynamic e = 4.5;
  e = 'reatribuindo uma String a um double';
}
```

#### Nullable Variable Declaration and Assignment (Declaração e atribuição de variável nulável)
```dart
void main() {
  TIPO? NOME = VALOR;

  bool? b = null;

  int? i = null;

  double? d = null;
  
  num? n = null;

  String? s = null;
  
  // também suporta variáveis dinâmicas qe aceitam qualqer tipo de valor, incluindo null e podem ser reatribuídas para outros tipos de valores. Object também pode ser usado
  dynamic? e = 4.5;
  e = 'reatribuindo uma String a um double';
}
```

#### late
```dart
void main() {
  // late pode ser usado em funções mas é desnecessário, ele somente é obrigatório em classes
  String s;
  s = 'qualqer coisa';
}
```
```dart
void main() {
  // mesmo como acima, mas o late é opcional em funções
  late String s;
  s = 'qualqer coisa';
}
```

## Concatenation (Concatenação)
```dart
void main() {
  String s = 'dart' + ' flutter ' + 20.toString();
}
```

## String Interpolation (Interpolação em String)
```dart
void main() {
  String s = 'dart flutter ${20}';
}
```

## Boolean Operators (Operadores Booleanos)
```dart
void main() {
  // Em uma cadeia de || (or):
  // - quando todos os valores são true, o resultado é true
  // - quando todos os valores são false, o resultado é false
  // - quando pelo menos 1 valor é true, o resultado é true

  // o || (or) pode ser associado à soma:
  // false || false == false assim como 0 + 0 = 0
  // false || true == true assim como 0 + 1 = 1
  // true || false == true assim como 1 + 0 = 1
  // true || true == true assim como 1 + 1 = 2
  bool or = false || false || false || true; // true
  
  // Em uma cadeia de && (and):
  // - quando todos os valores são true, o resultado é true
  // - quando todos os valores são false, o resultado é false
  // - quando pelo menos 1 valor é false, o resultado é false

  // o && (and) pode ser associado à multiplicação:
  // false && false == false assim como 0 * 0 = 0
  // false && true == false assim como 0 * 1 = 0
  // true && false == false assim como 1 * 0 = 0
  // true && true == true assim como 1 * 1 = 1
  bool and = true && true && true && false; // false
}
```
## Functions (Funções)
#### Function Definition (Definição de função)
```dart
  // Funções void não retornam nenhum valor, mas podem fazer qualqer tipo de operação em seu corpo
  void naoRetornaNada1() {
    int numero = 77;

    print('Exiba $numero na tela'); // quando esta função for chamada, 'Exiba 77 na tela' será mostrado
  }

  // Declaração de função com somente 1 instrução (linha), que não retorna nada. Arrow (seta)
  void naoRetornaNada1() => print('Esta função não pode retornar nada');
```

```dart
  bool booleana1() {
    bool b = false;
    
    return b;
  }
  
  // Declaração de função com somente 1 instrução (linha), que somente retorna. Arrow (seta)
  bool booleana2() => true;
```

```dart
  int numeroInteiro1() {
    int i = 65;

    return i;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna. Arrow (seta)
  int numeroInteiro2() => 45;
```

```dart
  double numeroRacional1() {
    double d = 5.7;

    return d;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna. Arrow (seta)
  double numeroRacional2() => 5.65;
```

```dart
  num numeroRacional1() {
    num n = 68.4;

    return n;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna. Arrow (seta)
  num numeroRacional2() => 9.82;
```

```dart
  String texto1() {
    String s = 'texto aleatório';

    return s;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna. Arrow (seta)
  String texto2() => 'texto retornado';
```

#### Function Calling (Chamada de função)
```dart
    NOME_DA_FUNÇÃO();

    // Exemplos usando as funções declaradas acima
    naoRetornaNada1(); // mostra na tela: 'Exiba 77 na tela'
    naoRetornaNada2(); // mostra na tela: 'Esta função não pode retornar nada'

    // as funções abaixo, não fazem nada na prática, pois a única coisa qe fazem é retornar um valor,
    // e uma chamada de função qe retorna um valor deve ser atribuída a uma variável ou usada dentro de outras funções, como a função print()
    booleana1();
    booleana2();
    numeroInteiro1();
    numeroInteiro2();
    numeroRacional1();
    numeroRacional2();
    texto1();
    texto2();
```

Para usar as chamadas de funções que retornam um valor, precisamos colocá-las dentro de outras funções, como a função print() ou atribuí-las a uma variável
```dart
    // atribuindo a uma variável
    TIPO_QUE_É_O_MESMO_DO_RETORNO_DA_FUNÇÃO NOME_DA_VARIÁVEL = NOME_DA_FUNÇÃO();

    // printando
    print(NOME_DA_FUNÇÃO());

    // Exemplos usando as funções declaradas acima

    // atribuindo a uma variável
    bool b1 = booleana1();

    // printando
    print(booleana1());

    // atribuindo a uma variável
    bool b2 = booleana2();

    // printando
    print(booleana2());

    // atribuindo a uma variável
    int i1 = numeroInteiro1();

    // printando
    print(numeroInteiro1());

    // atribuindo a uma variável
    int i2 = numeroInteiro2();

    // printando
    print(numeroInteiro2());

    // atribuindo a uma variável
    double d = numeroRacional1();

    // printando
    print(numeroRacional1());

    // atribuindo a uma variável
    num n = numeroRacional2();

    // printando
    print(numeroRacional2());

    // atribuindo a uma variável
    String s1 = texto1();

    // printando
    print(texto1());

    // atribuindo a uma variável
    String s2 = texto2();

    // printando
    print(texto2());
```

#### Optional parameters (Parâmetros Opcionais)
```dart
void f(int n, [int optional = 7]) {
  print('$n, $optional');
}

// na função g abaixo, como não foi atribuído um valor default (padrão) para optional, ocorrerá um erro na declaração da função
void g(int n, [int optional]) => print('$n, $optional');

// na função h abaixo, optional assumirá implicitamente um valor default (padrão) de null
void h(int n, [int? optional]) => print('$n, $optional');

void main() {
  f(2);    // quando não passado um valor, o valor default (padrão) é assumido
  f(3, 9); // agora passando um valor para o parâmetro opcional, o valor passado será assumido

  h(5);    // o segundo argumento (optional) terá o valor de null
}
```

#### Named parameters (Parâmetros Nomeados)
```dart
void f(int n, {int named = 7}) {
  print('$n, $named');
}

// na função g abaixo, como não foi atribuído um valor default (padrão) para named, ocorrerá um erro na declaração da função
void g(int n, {int named}) => print('$n, $optional');

// na função h abaixo, named assumirá implicitamente um valor default (padrão) de null
void h(int n, {int? named}) => print('$n, $optional');

// caso não se qeira atribuir um valor default (padrão), mas não se qeira permitir atribuir null para o parâmetro nomeado
// deve-se usar a keyword (palavra reservada) required, assim, será obrigatório atribuir um valor para o parâmetro nomeado
void l(int n, {required int named}) => print('$n, $optional');

void main() {
  f(2);           // quando não passado um valor, o valor default (padrão) é assumido
  f(3, named: 9); // agora passando um valor para o parâmetro nomeado, o valor passado será assumido

  h(5);           // o segundo argumento (named) terá o valor de null

  l(7, named: 10); // aqi é obrigatório passar um valor para o argumento nomeado (named) porqe ele foi definido como required
}
```

## Functions as first-class objects ou Functions as first-class citizens ou mais simples: atribuir uma função a uma variável
```dart
void main() {
  // atribuir função anônima (anonymous function) a variável
  int Function() f = () => 7 + 8;

  print(f()); // printará 15

  String Function() h = () { return 'Geraldo'; };

  print(h()); // printará 'Geraldo'
}
```

```dart
int g() => 8 + 9;

void main() {
  // atribuir função previamente declarada a variável
  int Function() f = g;

  print(f()); // printará 15
}
```

```dart
void main() {
  // na tipagem: em Function(int, int), dar nomes para os parâmetros é opcional, por exemplo: Function(int a, int b)
  // na atribuição de valor: em (a, b) => a + b; colocar a tipagem para os parâmetros é opcional, por exemplo: (int a, int b) => a + b;
  int Function(int, int) soma = (a, b) => a + b;

  print(soma(3, 7)); // printará 10
}
```

#### Parâmetros recebendo funções
```dart
void f(void Function() g) => g();

void main() {
  f(() => print('algo'));
}
```
```dart
// alternativamente, o parâmetro qe recebe a função pode ser escrito assim:
void f(void g()) => g();

void main() {
  f(() => print('algo'));
}
```

## class
```dart
// uma das formas de declarar uma class é inicializando seus atributos com valores padrões (default)
class Pessoa {
  String nome = 'Cleison';
  int idade = 54;
  num peso = 65.94;
}

void main() {
  Pessoa p = Pessoa();

  print(p.nome); // 'Cleiton'

  // alterando um dos atributos
  p.nome = 'Jailson';

  print(p.nome); // 'Jailson'
}
```

```dart
// outra forma é usando late para uma atribuição "tardia", "atrasada"
// no entanto, não atribuir um valor a qualqer atributo gerará um erro de compilação
class Pessoa {
  late String nome;
  late int idade;
  late num peso;
}

void main() {
  Pessoa p = Pessoa();
  p.nome = 'Cleiton';
  p.idade = 54;
  p.peso = 65.94;
  
  // alternativamente, pode atribuir usando uma sintaxe sugar, da seginte forma:
  p..nome = 'Cleiton';
    ..idade = 54;
    ..peso = 65.94;

  print(p.nome); // 'Cleiton'
}
```

### Constructors (Construtores)
```dart
// outra forma de inicializar uma instância de class é usando construtor
class Pessoa {
  late String nome;
  late int idade;
  late num peso;

  Pessoa(String nome, int idade, num peso) {
    this.nome = nome;
    this.idade = idade;
    this.peso = peso;
  }
}

void main() {
  Pessoa p = Pessoa('Cleitin', 49, 99.87);
  print(p.nome); // 'Cleitin'
}
```

```dart
// ou de forma mais simples e também mais usada: usando a syntax sugar para declaração do construtor
class Pessoa {
  String nome;
  int idade;
  num peso;

  Pessoa(this.nome, this.idade, this.peso);
}

void main() {
  Pessoa p = Pessoa('Cleitin', 49, 99.87);
  print(p.nome); // 'Cleitin'
}
```

### Inheritance (Herança)
```dart
class Pessoa {
  String nome;
  int idade;
  num peso;

  Pessoa(this.nome, this.idade, this.peso);

  void f() => print('Aluno herdará este método');

  void g() => print('Aluno também herdará este método');
}

class Aluno extends Pessoa {
  int idMatricula;

  Aluno(this.idMatricula, String nome, int idade, num peso) : super(nome, idade, peso);

  @override
  void g() => print('Este método será sobrescrito para Aluno');
}
```

## async, await, Future, then
```dart
Future<String> f() {
  return Future.delayed(const Duration(seconds: 5), () => 'delay');
}

// ou

Future<String> f() async {
  await Future.delayed(const Duration(seconds: 5));
  return 'delay';
}
```
```dart
void main() {
  print('antes');
  f().then((value) => print(value));
  print('depois');
}

void main() async {
  print('antes');
  print(await f());
  print('depois');
}
```
