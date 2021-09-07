## Tipos de dados
```dart
void main() {
  bool b = 2 != 4 || 7 == 7; // true

  int i = 4 + 10 * 5; // 54

  double d = 3 - 10 / 4; // 0.5
  
  num n = 4 + 7 / 8; // 4.875

  String s = 'texto ${2 + 3}' + ' concatecado'; // 'texto 5 concatecado'
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
