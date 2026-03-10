+++
date = '2026-03-09T18:13:54-03:00'
draft = false
math = true
title = 'First Post'
keywords = ['cap theorem', 'consistency']
toc = true
+++

That's my first post


{{< figure src="./cap-theorem.png" 
           caption="Figura 1 — Representação do CAP theorem"
           alt="CAP theorem diagram" >}}

Video:

{{< youtube 4Qy3jtXGPB4 >}}
*Vídeo 1: IA, ML, Deep Learning - Como as máquinas realmente aprendem?.*


A equação \(a^2 + b^2 = c^2\) aparece no meio do texto.


### 2.3 Equação de Einstein
---

\[
E = mc^2 \tag{1}
\]

---


### 2.4 Code Blocks

#### 2.4.1 Python Code

```python{hl_lines=[2],linenostart=1}
def soma(a, b):
    return a + b

def soma(a, b):
    return a + b
```

### 2.5 Link Redirect

Click [here](../distributed-systems/index.md) to go to Part 2.


### 2.6 Box Explicativo

#### 2.6.1 Hover the underlined expression below!
A teoria do <span title="Teorema que diz que sistemas distribuídos não podem garantir Consistency, Availability e Partition tolerance ao mesmo tempo"><u>CAP theorem</u></span> é fundamental.


### 2.7 Reference equation

Usar "\tag{1}" na equação.
Como vemos na equação 1, massa e energia são proporcionais.

### 2.8 CAP Thoerem

O **CAP Theorem** é um princípio fundamental em **sistemas distribuídos** que afirma que um sistema não pode garantir simultaneamente três propriedades desejáveis: **Consistência (Consistency)**, **Disponibilidade (Availability)** e **Tolerância a Partições (Partition Tolerance)**.

A **consistência** significa que todos os nós do sistema veem exatamente os mesmos dados ao mesmo tempo. Se um usuário grava um valor em um banco distribuído, qualquer leitura subsequente em qualquer nó deve retornar esse valor mais recente.

A **disponibilidade**, por outro lado, garante que o sistema sempre responda às requisições. Mesmo que algum nó esteja sobrecarregado ou falhe parcialmente, o sistema continua retornando respostas válidas para quem fizer requisições.

Já a **tolerância a partições** refere-se à capacidade do sistema continuar operando mesmo quando ocorre uma falha de comunicação entre partes da rede. Em outras palavras, se um conjunto de servidores perde a conexão com outro conjunto, cada lado ainda pode continuar funcionando.

O ponto central do teorema é que **quando ocorre uma partição de rede**, o sistema precisa escolher entre manter **consistência** ou **disponibilidade**. Se escolher consistência, algumas requisições podem ser rejeitadas para evitar retornar dados divergentes. Se escolher disponibilidade, o sistema continua respondendo, mas pode temporariamente devolver dados inconsistentes.

Esse princípio foi formulado por Eric Brewer no início dos anos 2000 e posteriormente formalizado por pesquisadores teóricos. Ele teve grande impacto no design de bancos de dados distribuídos e sistemas modernos de larga escala.

Por exemplo, bancos de dados como **Apache Cassandra** e **Amazon Dynamo** tendem a priorizar **disponibilidade e tolerância a partições**, aceitando consistência eventual. Já sistemas que priorizam consistência podem sacrificar disponibilidade durante falhas de rede.

Na prática, o teorema CAP não significa que apenas duas propriedades possam existir em um sistema. Em vez disso, ele destaca que **sob condições de partição**, é necessário fazer um trade-off entre consistência e disponibilidade — uma decisão arquitetural importante ao projetar sistemas distribuídos em larga escala.
