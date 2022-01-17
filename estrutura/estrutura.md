## Tipos de dados

#### Declaração e atribuição de variável
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

  // também suporta variáveis dinâmicas qe aceitam qualqer tipo de valor, incluindo null. Object também pode ser usado
  dynamic e = 4.5;
  e = 'reatribuindo uma String a um double';
}
```

#### Declaração e atribuição de variável nulável
```dart
void main() {
  TIPO? NOME = VALOR;

  bool? b = null;

  int? i = null;

  double? d = null;
  
  num? n = null;

  String? s = null;
  
  // também suporta variáveis dinâmicas qe aceitam qualqer tipo de valor, incluindo null. Object também pode ser usado
  dynamic? e = 4.5;
  e = 'reatribuindo uma String a um double';
}
```

## Concatenação
```dart
void main() {
  String s = 'dart' + ' flutter ' + 20.toString();
}
```

## Interpolação em String - String Interpolation
```dart
void main() {
  String s = 'dart flutter ${20}';
}
```

## Operadores booleanos
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
## Funções
#### Declaração de função
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

#### Chamada de função
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
    double numeroRacional1();
    
    // printando
    print(numeroRacional1());

    // atribuindo a uma variável
    num numeroRacional2();
    
    // printando
    print(numeroRacional2());

    // atribuindo a uma variável
    String texto1();
    
    // printando
    print(texto1());

    // atribuindo a uma variável
    String texto2();

    // printando
    print(texto2());
```

## 
