# Desafio-programa-o-gupy-

### 1) Valor da variável SOMA ao final do processamento:

```c
int INDICE = 13, SOMA = 0, K = 0;

while (K < INDICE) {
    K = K + 1;
    SOMA = SOMA + K;
}

printf("%d", SOMA);
```

Este código soma os números de 1 a 13 (1 + 2 + 3 + ... + 13). A soma final é:

**SOMA = 91**

### 2) Programa para verificar se um número pertence à sequência de Fibonacci:

 código em Python:

```python
def is_fibonacci(n):
    fib_a, fib_b = 0, 1
    while fib_a <= n:
        if fib_a == n:
            return True
        fib_a, fib_b = fib_b, fib_a + fib_b
    return False

# Exemplo de número a ser verificado
numero = 21

if is_fibonacci(numero):
    print(f"O número {numero} pertence à sequência de Fibonacci.")
else:
    print(f"O número {numero} não pertence à sequência de Fibonacci.")
```

Esse código verifica se um número informado (no exemplo, 21) pertence à sequência de Fibonacci.

### 3) Programa para calcular o menor, maior faturamento e dias acima da média:

Aqui está o código em Python:

```python
import json

# Exemplo de JSON com dados de faturamento diário
faturamento_diario_json = '''
{
    "faturamento": [1000, 1500, 0, 2000, 3000, 0, 2500, 1000, 500, 4000, 0, 1000]
}
'''

dados = json.loads(faturamento_diario_json)
faturamento = [f for f in dados["faturamento"] if f > 0]

menor_faturamento = min(faturamento)
maior_faturamento = max(faturamento)
media_mensal = sum(faturamento) / len(faturamento)

dias_acima_da_media = len([f for f in faturamento if f > media_mensal])

print(f"Menor faturamento: R${menor_faturamento}")
print(f"Maior faturamento: R${maior_faturamento}")
print(f"Dias acima da média: {dias_acima_da_media}")
```

Esse código calcula o menor, maior faturamento e o número de dias em que o faturamento foi superior à média mensal, considerando os dias sem faturamento.

### 4) Programa para calcular o percentual de faturamento por estado:

Aqui está o código em Python:

```python
faturamento = {
    "SP": 67836.43,
    "RJ": 36678.66,
    "MG": 29229.88,
    "ES": 27165.48,
    "Outros": 19849.53
}

total = sum(faturamento.values())

for estado, valor in faturamento.items():
    percentual = (valor / total) * 100
    print(f"{estado}: {percentual:.2f}%")
```

Esse código calcula e exibe o percentual de representação de cada estado dentro do valor total de faturamento mensal.

### 5) Programa para inverter uma string sem usar funções prontas:

Aqui está o código em Python:

```python
def inverter_string(s):
    string_invertida = ""
    for char in s:
        string_invertida = char + string_invertida
    return string_invertida

# Exemplo de string a ser invertida
string = "exemplo"
print(f"String invertida: {inverter_string(string)}")
```

Esse código inverte os caracteres de uma string sem utilizar funções prontas como `reverse()`.
