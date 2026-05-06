[for_java_em_5_linguagens.md](https://github.com/user-attachments/files/27419788/for_java_em_5_linguagens.md)
# Construção `for` de Java em 5 linguagens

## Enunciado

Escreva a seguinte construção `for` de Java em 5 Linguagens de Programação diferentes à sua escolha:

```java
int i, j, n = 100;

for (i = 0, j = 17; i < n; i++, j--)
  sum += i * j + 3;
```

---

# 1. C

```c
int i, j, n = 100;
int sum = 0;

for (i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
}
```

---

# 2. Ruby

```ruby
n = 100
sum = 0
j = 17

for i in 0...n
  sum += i * j + 3
  j -= 1
end
```

---

# 3. Dart

```dart
void main() {
  int n = 100;
  int sum = 0;

  for (int i = 0, j = 17; i < n; i++, j--) {
    sum += i * j + 3;
  }
}
```

---

# 4. PHP

```php
<?php
$n = 100;
$sum = 0;

for ($i = 0, $j = 17; $i < $n; $i++, $j--) {
    $sum += $i * $j + 3;
}
?>
```

---

# 5. Kotlin

```kotlin
fun main() {
    val n = 100
    var sum = 0
    var j = 17

    for (i in 0 until n) {
        sum += i * j + 3
        j--
    }
}
```

---

## Observação

Nas linguagens C, Dart e PHP, é possível escrever uma estrutura muito parecida com o `for` original de Java.

Em Ruby e Kotlin, a variável `j` foi atualizada dentro do corpo do laço, pois essas linguagens usam formas de repetição diferentes para percorrer intervalos.
