# 📅 Sistema Inteligente de Gestão de Tempo (Knapsack Optimization)

Este projeto apresenta um otimizador de gestão de tempo baseado no modelo clássico do Problema da Mochila 0/1, cuja finalidade é selecionar automaticamente as tarefas com maior valor dentro do limite de horas disponíveis no dia. Ideal para demonstração de raciocínio lógico, modelagem matemática e aplicações práticas de Programação Dinâmica.

---

## 🎯 Objetivo do Projeto

Criar um sistema que escolha as melhores tarefas do dia considerando:

- ⏳ Duração de cada tarefa  
- ⭐ Valor (importância / impacto)  
- 📆 Tempo total disponível (ex.: 8 horas)  

O algoritmo seleciona apenas as tarefas que maximizam o valor total, respeitando o limite de tempo.

---

## 🧠 Formulação Matemática

Cada tarefa i possui:

- dᵢ → duração  
- vᵢ → valor  
- xᵢ → decisão (0 = não escolher, 1 = escolher)

### Função objetivo  
Maximizar o valor total:

Σ(vᵢ · xᵢ)

### Restrição de tempo

Σ(dᵢ · xᵢ) ≤ T

Onde T é o limite de horas do usuário.

### Complexidade

O algoritmo usa Programação Dinâmica com complexidade:

O(n · T)

---

## 🛠 Tecnologias Utilizadas

- **Python**
- **NumPy**
- **Pandas**
- **Programação Dinâmica (DP)**

---

## 📚 Base de Dados

Tarefas utilizadas no estudo:

| Tarefa                | Duração | Valor |
|-----------------------|---------|-------|
| Estudar Python        | 2       | 5     |
| Exercícios Físicos    | 1       | 3     |
| Responder Emails      | 1       | 2     |
| Planejar Reunião      | 2       | 4     |
| Pesquisa de Mercado   | 3       | 6     |
| Ler Artigos           | 1       | 2     |
| Codificar Projeto     | 4       | 7     |
| Revisar Código        | 2       | 5     |
| Criar Apresentação    | 3       | 6     |
| Networking            | 2       | 4     |

---

## ✅ Resultado da Otimização

Com limite de **8 horas**, o algoritmo selecionou:

- Estudar Python — 2h — valor 5  
- Exercícios Físicos — 1h — valor 3  
- Responder Emails — 1h — valor 2  
- Planejar Reunião — 2h — valor 4  
- Revisar Código — 2h — valor 5  

**Valor total:** 19  
**Tempo utilizado:** 8h de 8h  

---

## 🧩 Funcionamento do Algoritmo

1. Monta-se uma matriz DP onde:
   - Linhas representam tarefas  
   - Colunas representam o tempo disponível  

2. Para cada célula, são comparadas duas situações:
   - **Incluir a tarefa** → se couber no tempo e aumentar o valor total  
   - **Excluir a tarefa** → manter o valor máximo anterior  

3. Ao final, realiza-se **backtracking** para identificar quais tarefas foram escolhidas.

---


