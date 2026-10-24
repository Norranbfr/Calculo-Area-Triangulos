# 📐 Cálculo da Área de Triângulos — Java

## 📌 Sobre o projeto

Projeto desenvolvido em **Java** para calcular e comparar as áreas de dois triângulos (X e Y), utilizando a **Fórmula de Heron**.

O programa recebe os três lados de cada triângulo, calcula suas áreas e identifica qual possui a maior área.

## 📐 Fórmula de Heron

O cálculo é realizado em duas etapas.

**1. Semiperímetro**

\[
p = \frac{a+b+c}{2}
\]

**2. Área do triângulo**

\[
A = \sqrt{p(p-a)(p-b)(p-c)}
\]

Onde `a`, `b` e `c` representam os lados, `p` é o semiperímetro e `A` é a área.

## 💻 Explicação passo a passo

**1. Importação das bibliotecas**

```java
import java.util.Locale;
import java.util.Scanner;
```

`Scanner` permite ler os valores digitados pelo usuário, enquanto `Locale` define o padrão dos números decimais.

**2. Entrada de dados**

```java
Scanner sc = new Scanner(System.in);
double xA, xB, xC, yA, yB, yC;
```

As variáveis armazenam os três lados de cada triângulo. O tipo `double` permite trabalhar com números decimais.

**3. Cálculo das áreas**

```java
double p = (xA + xB + xC) / 2.0;
double areaX = Math.sqrt(
    p * (p - xA) * (p - xB) * (p - xC)
);
```

O programa calcula o semiperímetro e aplica a Fórmula de Heron para encontrar a área do triângulo X. O mesmo processo é realizado para o triângulo Y.

**4. Exibição dos resultados**

```java
System.out.printf("Triangle X area: %.4f%n", areaX);
System.out.printf("Triangle Y area: %.4f%n", areaY);
```

O `printf()` exibe as áreas com quatro casas decimais.

**5. Comparação das áreas**

```java
if (areaX > areaY) {
    System.out.println("Larger area: X");
} else if (areaY > areaX) {
    System.out.println("Larger area: Y");
} else {
    System.out.println("The areas are equal");
}
```

A estrutura condicional identifica qual triângulo possui a maior área ou informa quando ambas são iguais.

## 🧠 Conceitos utilizados

- Variáveis e tipos de dados (`double`).
- Entrada de dados com `Scanner`.
- Operações matemáticas e `Math.sqrt()`.
- Formatação de saída com `printf()`.
- Estruturas condicionais (`if`, `else if` e `else`).

## 🚀 Conclusão

O projeto aplica conceitos fundamentais de Java na resolução de um problema matemático, exercitando lógica de programação, cálculos e estruturas de decisão.

**Observação:** para garantir resultados corretos, é importante validar se as medidas informadas formam triângulos válidos.
