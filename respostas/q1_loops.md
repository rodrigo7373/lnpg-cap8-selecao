[reescrita_pseudocodigo_lacos.md](https://github.com/user-attachments/files/27419722/reescrita_pseudocodigo_lacos.md)
# Reescrita de Pseudocódigo usando Estrutura de Laço

## Enunciado

Reescreva o seguinte segmento de pseudocódigo usando uma estrutura de laço nas linguagens especificadas:

```text
k = (j + 13) / 27

loop:
if k > 10 then goto out
  k = k + 1
  i = 3 * k - 1
  goto loop

out: ...
```

Linguagens:

a. Java  
b. Python  
c. Haskell  
d. Swift  

---

## a. Java

```java
int k = (j + 13) / 27;

while (k <= 10) {
    k = k + 1;
    i = 3 * k - 1;
}

// out: ...
```

---

## b. Python

```python
k = (j + 13) // 27

while k <= 10:
    k = k + 1
    i = 3 * k - 1

# out: ...
```

**Observação:** em Python, `//` representa divisão inteira.

---

## c. Haskell

```haskell
loop :: Int -> Int -> (Int, Int)
loop k i
  | k > 10 = (k, i)
  | otherwise =
      let kNovo = k + 1
          iNovo = 3 * kNovo - 1
      in loop kNovo iNovo

kInicial = (j + 13) `div` 27
(kFinal, iFinal) = loop kInicial i
```

**Observação:** em Haskell, a repetição normalmente é feita com recursão.

---

## d. Swift

```swift
var k = (j + 13) / 27

while k <= 10 {
    k = k + 1
    i = 3 * k - 1
}

// out: ...
```

---

## Explicação resumida

A lógica original usa `goto` para repetir o bloco enquanto `k` não for maior que `10`.

A condição:

```text
if k > 10 then goto out
```

foi transformada em:

```text
while k <= 10
```

Ou seja, enquanto `k <= 10`, o laço continua executando.  
Quando `k > 10`, o laço termina, equivalendo ao rótulo `out`.
