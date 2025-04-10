# Projeto 2 - Modelagem de Sistema de Manufatura com Redes de Petri Coloridas (CPN)

Este repositório contém a documentação e arquivos do Projeto 2 da disciplina de Sistemas a Eventos Discretos (SED), que consiste na modelagem de um sistema de manufatura com quatro células idênticas utilizando Redes de Petri Coloridas (CPN) na ferramenta **CPN Tools**.

---

## 🎯 Objetivo Geral

Modelar e validar um sistema de manufatura com múltiplas células, máquinas e robôs, utilizando Redes de Petri Coloridas para garantir funcionamento correto e sem bloqueios (deadlocks). O modelo é hierárquico, com temporizações e análises de desempenho.

---

## 🏭 Descrição do Sistema

O sistema é composto por **4 células idênticas**, cada uma contendo:

- 1 Depósito de Entrada Principal.
- 1 Depósito de Saída Principal.
- 3 Máquinas de processamento (M1, M2, M3).
- 3 Robôs (R1, R2, R3).

Cada máquina possui depósitos próprios de entrada e saída. A movimentação de itens é realizada da seguinte forma:

- **Robô 1 (R1):** Transporta itens do depósito de entrada da célula para a entrada da Máquina 1.
- **Robô 2 (R2):** Leva itens da saída da Máquina 1 para a entrada das Máquinas 2 ou 3, dependendo da rota (i ou j).
- **Robô 3 (R3):** Leva itens da saída das Máquinas 2 e 3 para o depósito de saída da célula.

Cada célula executa duas possíveis rotas de produção:
- **Rota i:** M1 → M2 → Saída.
- **Rota j:** M1 → M3 → Saída.

---

## 🧠 Modelagem no CPN Tools

- Modelo implementado com **Redes de Petri Coloridas**.
- Estrutura **hierárquica**: cada célula é um módulo reutilizável.
- Utilização de **color sets** para representar itens, rotas, células e atributos dos tokens.
- Inclusão de **tempo (timestamps)** para representar atrasos de transporte e processamento.
- Limite de **4 tokens por depósito** para simular a capacidade máxima.

---

## 🧪 Análise de Desempenho

Foram utilizados **monitores** no CPN Tools para avaliar:

- Ocorrência de deadlocks.
- Tempo médio de processamento por célula.
- Filas nos depósitos.
- Utilização dos robôs e máquinas.
- Vazão (throughput) do sistema.

---

## 🖼️ Visualizações e Validações

- O modelo inclui visualizações do funcionamento das células.
- Foram aplicadas simulações com diferentes configurações para validar a ausência de bloqueios e a consistência do sistema.
- Foram utilizados **Message Sequence Charts (MSC)** e visualizações gráficas com a ferramenta **BRITNeY** integrada ao CPN Tools.

---

## 📁 Estrutura do Repositório

```
📦 Projeto_SED_CPN
 ┣ 📁 models
 ┃ ┣ 📄 projeto_cpn_final.cpnet
 ┃ ┗ 📄 celula_subpage.cpnet
 ┣ 📁 imagens
 ┃ ┣ 📄 diagrama_estrutura.png
 ┃ ┗ 📄 msc_simulacao.png
 ┣ 📄 README.md
 ┗ 📄 relatorio_projeto2.pdf
```

---

## 🎬 Demonstração em Vídeo

[🔗 Clique aqui para assistir ao vídeo explicativo no YouTube](https://youtu.be/SEU_VIDEO_AQUI)

---

## 👨‍💻 Desenvolvedor

- **Nome:** [Seu Nome Aqui]
- **Curso:** Engenharia Elétrica / Computação
- **Universidade:** Universidade Federal de Campina Grande (UFCG)
- **Email:** seu.email@exemplo.com

---

## 📫 Contato do Professor

- **Prof. Kyller Costa Gonçalves**
- **Email:** kyller@dee.ufcg.edu.br

---

## 🛠️ Ferramentas Utilizadas

- [CPN Tools](https://cpntools.org)
- [Java Runtime](https://www.java.com)
- Git e GitHub para versionamento e documentação.

---

## ✅ Requisitos Atendidos

- [x] Modelo hierárquico funcional com 4 células.
- [x] Uso de CPN ML para definir color sets e expressões.
- [x] Simulação e análise com monitores.
- [x] Relatório documentado.
- [x] Vídeo explicativo no tempo limite de 8 minutos.
- [x] Compartilhamento via GitHub com permissão para o professor.

---

## 📎 Licença

Este projeto é parte de um trabalho acadêmico e não possui fins comerciais.