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
  bool or = false || false || false || true; // true
  bool and = true && true && true && false; // false
}
```
## Funções
#### Declaração de função
```dart
  bool booleana1() {
    bool b = false;
    
    return b;
  }
  
  // Declaração de função com somente 1 instrução (linha), que somente retorna
  bool booleana2() => true;
```

```dart
  int numeroInteiro1() {
    int i = 65;

    return i;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna
  int numeroInteiro2() => 45;
```

```dart
  double numeroRacional1() {
    double d = 5.7;

    return d;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna
  double numeroRacional2() => 5.65;
```

```dart
  num numeroRacional1() {
    num n = 68.4;

    return n;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna
  num numeroRacional2() => 9.82;
```

```dart
  String texto1() {
    String s = 'texto aleatório';

    return s;
  }

  // Declaração de função com somente 1 instrução (linha), que somente retorna
  String texto2() => 'texto retornado';
```

#### Chamada de função
```dart
    NOME_DA_FUNÇÃO();
    
    // Exemplos usando as funções declaradas acima
    booleana1();
    booleana2();
    numeroInteiro1();
    numeroInteiro2();
    numeroRacional1();
    numeroRacional2();
    texto1();
    texto2();
```

Para usar as chamadas de funções, precisamos colocá-las em um print() ou atribuí-las a uma variável
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
