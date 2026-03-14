# python-ai-codes

# 🐍 Atividade Prática — IA Generativa com Python

> Atividade desenvolvida com o auxílio de IA Generativa para geração e explicação de códigos Python.  
> Todos os códigos foram testados no **Google Colab**.

---

## 📋 Índice

- [Exercício 1 — Média de 4 valores](#exercício-1--média-de-4-valores)
- [Exercício 2 — Tabuada do 1 ao 10](#exercício-2--tabuada-do-1-ao-10)
- [Exercício 3 — Pesquisa: statistics e numpy](#exercício-3--pesquisa-statistics-e-numpy)
- [Exercício 4 — Mediana com statistics](#exercício-4--mediana-com-statistics)
- [Exercício 5 — Pesquisa: Desvio Padrão](#exercício-5--pesquisa-desvio-padrão)
- [Exercício 6 — Desvio Padrão com numpy](#exercício-6--desvio-padrão-com-numpy)
- [Exercício 7 — Amplitude em Estatística](#exercício-7--amplitude-em-estatística)
- [Exercício 8 — Análise Preditiva de Ar Condicionado](#exercício-8--análise-preditiva-de-ar-condicionado)

---

## Exercício 1 — Média de 4 valores

### 📌 Descrição
Calcular a **média aritmética** de 4 valores e explicar cada linha do código.

### 💻 Código

```python
# Definindo os 4 valores
valores = [8, 6, 9, 7]

# Somando todos os valores da lista
soma = sum(valores)

# Dividindo a soma pela quantidade de elementos
media = soma / len(valores)

# Exibindo o resultado
print("Média:", media)
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `valores = [8, 6, 9, 7]` | Cria uma lista com 4 números |
| `soma = sum(valores)` | Soma todos os elementos da lista |
| `media = soma / len(valores)` | Divide a soma pela quantidade de elementos (4) |
| `print("Média:", media)` | Exibe o resultado na tela |

### ✅ Saída esperada
```
Média: 7.5
```

---

## Exercício 2 — Tabuada do 1 ao 10

### 📌 Descrição
Gerar a **tabuada do 1 ao 10** e explicar cada linha do código.

### 💻 Código

```python
# Laço que percorre os números de 1 a 10
for numero in range(1, 11):

    # Exibe o título de cada tabuada
    print(f"\nTabuada do {numero}:")

    # Laço interno para multiplicar de 1 a 10
    for i in range(1, 11):

        # Calcula e exibe o resultado da multiplicação
        print(f"{numero} x {i} = {numero * i}")
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `for numero in range(1, 11)` | Itera de 1 até 10 (o 11 é exclusivo) |
| `f"\nTabuada do {numero}:"` | F-string que formata o texto com o número atual |
| `for i in range(1, 11)` | Segundo laço que vai de 1 a 10 |
| `numero * i` | Realiza a multiplicação |
| `print(...)` | Exibe cada linha da tabuada |

### ✅ Saída esperada
```
Tabuada do 1:
1 x 1 = 1
1 x 2 = 2
...
Tabuada do 10:
10 x 9 = 90
10 x 10 = 100
```

---

## Exercício 3 — Pesquisa: statistics e numpy

### 📌 Descrição
Pesquisa sobre as bibliotecas **statistics** e **numpy**.

---

### 📚 Biblioteca `statistics`

É uma biblioteca **nativa do Python** (não precisa instalar). Fornece funções para cálculos estatísticos básicos como média, mediana, moda e desvio padrão. Ideal para conjuntos de dados simples.

| Função | Descrição |
|--------|-----------|
| `statistics.mean()` | Média aritmética |
| `statistics.median()` | Mediana |
| `statistics.mode()` | Moda |
| `statistics.stdev()` | Desvio padrão amostral |
| `statistics.pstdev()` | Desvio padrão populacional |

---

### 📚 Biblioteca `numpy`

É uma biblioteca **externa** (instalada via `pip install numpy`). Uma das mais usadas em ciência de dados e computação científica. Trabalha com arrays multidimensionais de alta performance e oferece funções matemáticas avançadas.

| Função | Descrição |
|--------|-----------|
| `numpy.mean()` | Média |
| `numpy.median()` | Mediana |
| `numpy.std()` | Desvio padrão |
| `numpy.array()` | Cria arrays |
| `numpy.sum()` | Soma os elementos |

---

## Exercício 4 — Mediana com statistics

### 📌 Descrição
Calcular a **mediana** utilizando a biblioteca `statistics` e explicar cada linha do código.

### 💻 Código

```python
# Importando a biblioteca statistics
import statistics

# Definindo o conjunto de valores
valores = [4, 8, 15, 16, 23, 42]

# Calculando a mediana
mediana = statistics.median(valores)

# Exibindo o resultado
print("Mediana:", mediana)
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `import statistics` | Importa a biblioteca padrão do Python para estatística |
| `valores = [...]` | Cria a lista de números a ser analisada |
| `statistics.median(valores)` | Ordena os valores automaticamente e retorna o valor central |
| `print(...)` | Exibe a mediana calculada |

> 💡 Se a lista tiver quantidade **par** de elementos, a mediana é a média dos dois valores centrais.

### ✅ Saída esperada
```
Mediana: 15.5
```

---

## Exercício 5 — Pesquisa: Desvio Padrão

### 📌 Descrição
Pesquisa sobre o conceito de **desvio padrão** em estatística.

### 📐 O que é Desvio Padrão?

O **desvio padrão** é uma medida estatística que indica o quanto os valores de um conjunto de dados se **afastam da média**.

- Desvio padrão **baixo** → valores **concentrados** próximos à média
- Desvio padrão **alto** → valores **dispersos** / espalhados

### Fórmula

```
σ = √( Σ(xᵢ - x̄)² / n )
```

Onde:
- `xᵢ` = cada valor do conjunto
- `x̄` = média dos valores
- `n` = quantidade de valores

### Exemplo prático

| Conjunto | Desvio Padrão | Interpretação |
|----------|---------------|---------------|
| `[10, 10, 10, 10]` | 0 | Todos iguais, sem dispersão |
| `[2, 5, 8, 14]` | ~4,5 | Valores mais espalhados |

### Tipos de Desvio Padrão

| Tipo | Símbolo | Uso |
|------|---------|-----|
| Amostral | s | Dados representam uma **amostra** |
| Populacional | σ | Dados representam a **população inteira** |

---

## Exercício 6 — Desvio Padrão com numpy

### 📌 Descrição
Calcular o **desvio padrão** de um conjunto de números utilizando a biblioteca `numpy` e explicar cada linha do código.

### 💻 Código

```python
# Importando a biblioteca numpy com o apelido "np"
import numpy as np

# Definindo o conjunto de números
numeros = [12, 7, 3, 14, 6, 11, 5, 8]

# Convertendo a lista para um array numpy
array_numeros = np.array(numeros)

# Calculando a média do conjunto
media = np.mean(array_numeros)

# Calculando o desvio padrão populacional
desvio_padrao = np.std(array_numeros)

# Exibindo os resultados
print("Conjunto:", numeros)
print("Média:", media)
print("Desvio Padrão:", desvio_padrao)
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `import numpy as np` | Importa o numpy com o apelido `np` |
| `numeros = [...]` | Lista com os dados a serem analisados |
| `np.array(numeros)` | Converte a lista em array numpy para cálculos mais eficientes |
| `np.mean(array_numeros)` | Calcula a média aritmética de todos os elementos |
| `np.std(array_numeros)` | Calcula o desvio padrão populacional por padrão |
| `print(...)` | Exibe os resultados formatados |

### ✅ Saída esperada
```
Conjunto: [12, 7, 3, 14, 6, 11, 5, 8]
Média: 8.25
Desvio Padrão: 3.49...
```

---

## Exercício 7 — Amplitude em Estatística

### 📌 Descrição
Pesquisa sobre **Amplitude** em estatística e exemplo com lista de dados.

### 📊 O que é Amplitude?

A **amplitude** (ou amplitude total) é a medida de dispersão mais simples, representando a diferença entre o **maior** e o **menor** valor de um conjunto de dados.

```
Amplitude = Valor máximo − Valor mínimo
```

### 💻 Código

```python
# Importando numpy para auxiliar nos cálculos
import numpy as np

# Definindo uma lista de dados (ex: temperaturas registradas em um dia)
dados = [22, 35, 18, 40, 27, 33, 15, 38, 25, 30]

# Encontrando o valor máximo da lista
valor_maximo = np.max(dados)

# Encontrando o valor mínimo da lista
valor_minimo = np.min(dados)

# Calculando a amplitude
amplitude = valor_maximo - valor_minimo

# Exibindo os resultados
print("Dados:", dados)
print("Valor máximo:", valor_maximo)
print("Valor mínimo:", valor_minimo)
print("Amplitude:", amplitude)
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `dados = [...]` | Lista com os valores registrados |
| `np.max(dados)` | Retorna o maior valor do conjunto |
| `np.min(dados)` | Retorna o menor valor do conjunto |
| `amplitude = valor_maximo - valor_minimo` | Subtrai o mínimo do máximo para obter a variação total |
| `print(...)` | Exibe cada parte do resultado |

### ✅ Saída esperada
```
Dados: [22, 35, 18, 40, 27, 33, 15, 38, 25, 30]
Valor máximo: 40
Valor mínimo: 15
Amplitude: 25
```

---

## Exercício 8 — Análise Preditiva de Ar Condicionado

### 📌 Descrição
Realizar a **análise preditiva** do funcionamento de um ar condicionado em um determinado ambiente, utilizando desvio padrão e amplitude.

### 💻 Código

```python
# Importando as bibliotecas necessárias
import numpy as np
import statistics

# -----------------------------------------------
# DADOS SIMULADOS: temperaturas registradas no ambiente
# ao longo de 15 dias (em graus Celsius)
# -----------------------------------------------
temperaturas = [28, 30, 35, 33, 29, 36, 38, 31,
                27, 34, 37, 32, 30, 39, 26]

# Convertendo para array numpy
dados = np.array(temperaturas)

# -----------------------------------------------
# CÁLCULOS ESTATÍSTICOS
# -----------------------------------------------

# Calculando a média das temperaturas
media = np.mean(dados)

# Calculando a mediana
mediana = np.median(dados)

# Calculando o desvio padrão (dispersão em relação à média)
desvio_padrao = np.std(dados)

# Calculando a amplitude (variação total das temperaturas)
amplitude = np.max(dados) - np.min(dados)

# -----------------------------------------------
# ANÁLISE PREDITIVA
# -----------------------------------------------

# Limite de temperatura segura para o ar condicionado
limite_critico = media + (1.5 * desvio_padrao)

# Verificando quantos dias ultrapassaram o limite crítico
dias_criticos = sum(1 for t in temperaturas if t > limite_critico)

# -----------------------------------------------
# EXIBINDO OS RESULTADOS
# -----------------------------------------------
print("=" * 45)
print("  ANÁLISE PREDITIVA - AR CONDICIONADO")
print("=" * 45)
print(f"Temperaturas registradas: {temperaturas}")
print(f"Média das temperaturas  : {media:.2f} °C")
print(f"Mediana                 : {mediana:.2f} °C")
print(f"Desvio Padrão           : {desvio_padrao:.2f} °C")
print(f"Amplitude               : {amplitude:.2f} °C")
print(f"Limite crítico (predito): {limite_critico:.2f} °C")
print(f"Dias acima do limite    : {dias_criticos} dia(s)")
print("=" * 45)

# Diagnóstico preditivo
if dias_criticos > 3:
    print("⚠️  ALERTA: Alta demanda sobre o ar condicionado!")
    print("   Recomenda-se revisão preventiva do equipamento.")
elif dias_criticos > 0:
    print("⚡ ATENÇÃO: Alguns picos de temperatura detectados.")
    print("   Monitoramento contínuo recomendado.")
else:
    print("✅ NORMAL: Temperatura dentro dos parâmetros esperados.")
```

### 🔍 Explicação

| Linha | Descrição |
|-------|-----------|
| `import numpy as np` | Importa o numpy para cálculos estatísticos eficientes |
| `temperaturas = [...]` | Simula dados coletados por sensores ao longo de 15 dias |
| `np.array(dados)` | Converte a lista em array numpy para processamento otimizado |
| `np.mean(dados)` | Calcula a temperatura média do período |
| `np.median(dados)` | Calcula a mediana (valor central dos dados ordenados) |
| `np.std(dados)` | Calcula o desvio padrão — indica a variabilidade da temperatura |
| `np.max() - np.min()` | Calcula a amplitude (diferença entre maior e menor temperatura) |
| `limite_critico = media + (1.5 * desvio_padrao)` | Define o **limite preditivo** de sobrecarga do equipamento |
| `sum(1 for t in temperaturas if t > limite_critico)` | Conta quantos dias ultrapassaram o limite crítico |
| Blocos `if/elif/else` | Emitem um **diagnóstico automático** baseado nos dados analisados |

### ✅ Saída esperada
```
=============================================
  ANÁLISE PREDITIVA - AR CONDICIONADO
=============================================
Temperaturas registradas: [28, 30, 35, 33, 29, 36, 38, 31, 27, 34, 37, 32, 30, 39, 26]
Média das temperaturas  : 32.33 °C
Mediana                 : 32.00 °C
Desvio Padrão           : 3.92 °C
Amplitude               : 13.00 °C
Limite crítico (predito): 38.21 °C
Dias acima do limite    : 1 dia(s)
=============================================
⚡ ATENÇÃO: Alguns picos de temperatura detectados.
   Monitoramento contínuo recomendado.
```

---

## 🛠️ Tecnologias Utilizadas

- **Python 3.x**
- **Google Colab**
- **Biblioteca `statistics`** (nativa do Python)
- **Biblioteca `numpy`** (instalação: `pip install numpy`)

---

## 📖 Referências

- [Google Colab](https://colab.google/)
- [Documentação NumPy](https://numpy.org/doc/)
- [Documentação statistics — Python](https://docs.python.org/3/library/statistics.html)
- [Tom M. Mitchell — Wikipedia](https://en.wikipedia.org/wiki/Tom_M._Mitchell)

---

> *"A visão de IA de Tom Mitchell coloca o aprendizado de máquina no centro da construção de sistemas inteligentes, onde a habilidade de aprender a partir de dados e melhorar com a experiência é fundamental."*  
> **(Mitchell) (Gerado por IA)**
