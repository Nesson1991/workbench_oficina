# Construindo um Esquema Conceitual para Banco de Dados - Oficina Mecânica

![Diagrama ER - Oficina Mecânica](https://github.com/Nesson1991/workbench_oficina/blob/main/Oficina%20Mec%C3%A2nica.png?raw=true)

Este repositório contém o projeto desenvolvido para construir um esquema conceitual de banco de dados, focado no **Sistema de Controle e Gerenciamento de Execução de Ordens de Serviço (OS)** de uma oficina mecânica.

## 💡 Descrição do Projeto

O projeto tem como objetivo modelar o fluxo de trabalho de uma oficina mecânica, desde a entrada do veículo até a conclusão dos serviços. Através de um banco de dados relacional, é possível gerenciar as **ordens de serviço (OS)**, **mecânicos**, **clientes** e **serviços** realizados na oficina.

### 📌 Narrativa Utilizada:

- **Clientes** levam veículos à oficina para serem **consertados** ou para passarem por **revisões periódicas**.
- Cada **veículo** é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma **Ordem de Serviço (OS)** com a **data de entrega**.
- A partir da **OS**, calcula-se o valor de cada serviço, consultando-se uma **tabela de referência de mão-de-obra**.
- O valor de cada peça também compõe a **OS**.
- O cliente autoriza a execução dos serviços.
- A mesma equipe avalia e executa os serviços.
- **Mecânicos** possuem: **código**, **nome**, **endereço** e **especialidade**.
- Cada **OS** possui: **número**, **data de emissão**, **valor**, **status** e uma **data para conclusão** dos trabalhos.

## 🔧 Detalhes do Modelo

### Entidades Principais:
- **Clientes**: responsáveis por trazer os veículos para a oficina.
- **Veículos**: cada cliente pode ter mais de um veículo.
- **Mecânicos**: responsáveis pela execução dos serviços.
- **Serviços**: identificados e atribuídos a uma OS.
- **Peças**: adicionadas à OS conforme necessário.

### Relacionamentos:
- **Cliente** possui um ou mais **veículos**.
- **Veículo** recebe uma **ordem de serviço (OS)**, associada a uma **equipe de mecânicos**.
- **OS** inclui um ou mais **serviços** e **peças**.

## 🛠️ Ferramentas Utilizadas

- **MySQL Workbench**: ferramenta para modelagem do banco de dados.
- **MySQL**: banco de dados utilizado para implementar a modelagem.

## 📂 Estrutura do Projeto

O repositório contém:
- O arquivo de **modelagem visual** gerado no MySQL Workbench (.mwb);
- Script SQL para **criação das tabelas** e dos relacionamentos entre elas.

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repositorio.git
