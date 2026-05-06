[reescrita_sem_c_sem_goto_break.md](https://github.com/user-attachments/files/27420087/reescrita_sem_c_sem_goto_break.md)
# Reescrita sem `goto` ou `break` em 3 linguagens

## Enunciado

Considere o seguinte segmento de programa em C. Reescreva-o sem usar `goto` ou `break` em 3 linguagens diferentes à sua escolha.

```c
j = -3;

for (i = 0; i < 3; i++) {
  switch (j + 2) {
    case 3:
    case 2:
      j--;
      break;

    case 0:
      j += 2;
      break;

    default:
      j = 0;
  }

  if (j > 0)
    break;

  j = 3 - i;
}
```

> Observação: no código original, faltava `;` em `j = 3 - i`.

---

## 1. Python

```python
i = 0
j = -3
sair = False

while i < 3 and not sair:
    if j + 2 == 3 or j + 2 == 2:
        j -= 1
    elif j + 2 == 0:
        j += 2
    else:
        j = 0

    if j > 0:
        sair = True
    else:
        j = 3 - i
        i += 1

print("i =", i)
print("j =", j)
```

---

## 2. Java

```java
public class Main {
    public static void main(String[] args) {
        int i = 0;
        int j = -3;
        boolean sair = false;

        while (i < 3 && !sair) {
            if (j + 2 == 3 || j + 2 == 2) {
                j--;
            } else if (j + 2 == 0) {
                j += 2;
            } else {
                j = 0;
            }

            if (j > 0) {
                sair = true;
            } else {
                j = 3 - i;
                i++;
            }
        }

        System.out.println("i = " + i);
        System.out.println("j = " + j);
    }
}
```

---

## 3. Ruby

```ruby
i = 0
j = -3
sair = false

while i < 3 && !sair
  if j + 2 == 3 || j + 2 == 2
    j -= 1
  elsif j + 2 == 0
    j += 2
  else
    j = 0
  end

  if j > 0
    sair = true
  else
    j = 3 - i
    i += 1
  end
end

puts "i = #{i}"
puts "j = #{j}"
```

---

## Explicação resumida

O `switch` original foi substituído por estruturas de decisão `if`, `else if` ou `elsif`.

O `break` usado para sair do laço foi substituído por uma variável de controle chamada `sair`.

Assim, o laço continua enquanto:

```text
i < 3 e sair == falso
```

Quando `j > 0`, a variável `sair` recebe verdadeiro, encerrando o laço sem usar `break`.
