# 📈 Análise Estatística — Melhoria da Experiência do Cliente em Rede de Supermercados

## ❗ Desafio Apresentado

Uma grande rede de supermercados do país, atua com mais de 150 lojas em todo o território nacional, atendendo milhares de clientes diariamente. Com foco na excelência do atendimento, a empresa busca constantemente otimizar processos internos e garantir uma experiência de compra eficiente, rápida e satisfatória para seus clientes.
Está enfrentando desafios com o atendimento ao cliente. As reclamações mais comuns são sobre o **tempo de espera nas filas dos caixas** e a **disponibilidade de funcionários para ajudar os clientes**. A empresa decidiu realizar uma **pesquisa abrangente** para entender melhor esses problemas e encontrar maneiras de melhorar a **experiência do cliente**.

Diante disso, nossa equipe de consultoria foi acionada para realizar uma **análise estatística exploratória** com o objetivo de identificar padrões, gargalos e oportunidades de melhoria com base em dados coletados em múltiplas lojas da rede.

---

## 🎯 Objetivos da Análise

1. **Descrever e entender o comportamento dos tempos de espera.**
2. **Avaliar a relação entre tempo de espera e satisfação dos clientes.**
3. **Identificar outliers e eventos atípicos.**
4. **Calcular a probabilidade de tempos de espera excessivos.**
5. **Comparar o desempenho de lojas que adotaram uma nova política de atendimento.**
6. **Apoiar decisões baseadas em evidências com recomendações objetivas.**

---

## 🧾 Dados Disponibilizados

A análise foi realizada com base nos seguintes conjuntos de dados, coletados durante uma semana, em múltiplas lojas e horários:

| Variável                | Descrição                                                                 |
|-------------------------|---------------------------------------------------------------------------|
| `tempo_espera`          | Tempo de espera na fila do caixa (em minutos).                            |
| `satisfacao`            | Nota dada pelo cliente após atendimento (escala de 1 a 10).               |
| `num_funcionarios`      | Número de funcionários disponíveis por turno.                             |
| `clientes_por_hora`     | Volume de clientes por hora durante o período analisado.                  |
| `politica_nova`         | Flag indicando se a loja utiliza a nova política de atendimento (0 ou 1). |

---

## 🧪 Metodologia Estatística

### 1. **Estatística Descritiva**

Foram calculadas **medidas de tendência central** (média, mediana) e **dispersão** (desvio padrão) para entender a distribuição do tempo de espera e da satisfação dos clientes. 

- **Média tempo de espera**: ~7 minutos.
- **Desvio padrão**: ~2 minutos.
- **Média satisfação**: ~3.7 pontos.

---

### 2. **Identificação de Outliers**

Utilizamos:

- **Z-Score**: Para detectar valores com desvios superiores a 3 sigmas da média.
- **Boxplots**: Para visualização gráfica de valores extremos.

> **Impacto dos outliers**: Podem distorcer médias e regressões. Em alguns casos, foram considerados ruídos (erros de registro), e removidos para manter a robustez dos resultados.

---

### 3. **Correlação**

Foi medida a **correlação de Pearson** entre `tempo_espera` e `satisfacao`.

- Resultado: **-0.0966**  
> Indica uma **correlação negativa fraca**, ou seja, quanto maior o tempo de espera, **tende a diminuir levemente a satisfação**, embora o efeito seja sutil.

---

### 4. **Regressão Linear**

Modelamos a relação entre tempo de espera e satisfação por meio de **regressão linear simples**:

- Inclinação: **-0.7657**
- Intercepto: **8.7873**

> Cada minuto adicional de espera reduz em média **0.76 pontos** na nota de satisfação do cliente.

---

### 5. **Probabilidade de Espera Excedente**

Com base na distribuição normal do tempo de espera:

- Probabilidade de um cliente esperar **mais de 10 minutos**: **20.48%**

> Este valor indica que **1 em cada 5 clientes** enfrenta um tempo de espera crítico, reforçando a necessidade de intervenção operacional.

---

### 6. **Comparação entre Políticas**

Foram analisadas duas amostras:
- Lojas com **política de atendimento tradicional**.
- Lojas que implementaram a **nova política de atendimento**.

Realizamos testes estatísticos:
- **Teste t de Student** (variância semelhante)
- **Teste de Mann-Whitney** (não-paramétrico)

> Resultado: **sem evidência estatisticamente significativa** de melhoria na nova política, sugerindo que:
  - A implementação pode estar mal conduzida.
  - O período de coleta pode ter sido curto.
  - Outras variáveis ocultas podem interferir.

---

## 📌 Conclusões

- Há **alta variabilidade** no tempo de espera, com casos de espera acima de 10 minutos ocorrendo em **20%** dos registros.
- Pequenas variações no tempo de espera **impactam diretamente na satisfação**.
- A **nova política ainda não apresenta resultados conclusivos** em termos de desempenho.
- **Outliers** devem ser controlados para garantir análises consistentes.

---

## ✅ Recomendações Estratégicas

1. **Redesenhar a política de atendimento**, com foco nos horários de pico.
2. **Aumentar a equipe nos turnos críticos**, de acordo com análise do fluxo de clientes por hora.
3. **Implementar um sistema de triagem ou caixas rápidos** para reduzir o tempo médio de espera.
4. **Reavaliar a nova política de atendimento**, garantindo treinamento adequado dos colaboradores.
5. **Monitoramento contínuo com dashboards analíticos**, para acompanhamento em tempo real.

---

## 💻 Ferramentas Utilizadas

- Python
- Pandas
- Scikit-learn
- Scipy
- Matplotlib / Seaborn
- Google Colab

---

## 🧑‍💼 Sobre a Consultoria

Este projeto foi conduzido por [**AlmeidaTI**], especializado em:
- Inteligência analítica para varejo
- Diagnóstico estatístico de processos operacionais
- Modelagem preditiva e suporte à tomada de decisão

📧 **Contato:** contato@suaempresa.com  
🌐 **Website:** www.suaconsultoria.com.br

---
