[selecao_multipla_c_ruby_erlang.md](https://github.com/user-attachments/files/27419763/selecao_multipla_c_ruby_erlang.md)
# Reescrita usando Sentença de Seleção Múltipla

## Enunciado

Reescreva o seguinte segmento de código usando uma sentença de seleção múltipla nas seguintes linguagens:

```text
if ((k == 1) || (k == 2)) j = 2 * k - 1
if ((k == 3) || (k == 5)) j = 3 * k + 1
if (k == 4) j = 4 * k - 1
if ((k == 6) || (k == 7) || (k == 8)) j = k - 2
```

Linguagens:

a. C  
b. Ruby  
c. Erlang  

---

## a. C

```c
switch (k) {
    case 1:
    case 2:
        j = 2 * k - 1;
        break;

    case 3:
    case 5:
        j = 3 * k + 1;
        break;

    case 4:
        j = 4 * k - 1;
        break;

    case 6:
    case 7:
    case 8:
        j = k - 2;
        break;
}
```

---

## b. Ruby

```ruby
case k
when 1, 2
  j = 2 * k - 1
when 3, 5
  j = 3 * k + 1
when 4
  j = 4 * k - 1
when 6, 7, 8
  j = k - 2
end
```

---

## c. Erlang

```erlang
J =
    case K of
        1 -> 2 * K - 1;
        2 -> 2 * K - 1;
        3 -> 3 * K + 1;
        5 -> 3 * K + 1;
        4 -> 4 * K - 1;
        6 -> K - 2;
        7 -> K - 2;
        8 -> K - 2
    end.
```

---

## Observação

Em C usamos `switch`.

Em Ruby usamos `case`.

Em Erlang usamos `case ... of`.
