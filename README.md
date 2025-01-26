Sistema de Controle e Gerenciamento de Ordens de Serviço para Oficina Mecânica

Descrição do Projeto

Este projeto propõe um esquema conceitual para um sistema de controle e gerenciamento de ordens de serviço em uma oficina mecânica. O objetivo é organizar e detalhar as informações relacionadas a clientes, veículos, ordens de serviço, equipes, mecânicos, serviços e peças, facilitando o fluxo de trabalho e o cálculo de valores associados.

O esquema foi desenvolvido com base na narrativa fornecida e segue boas práticas de modelagem de banco de dados relacional.

Entidades e Relacionamentos

Entidades

Cliente

Código (PK)

Nome

Endereço

Telefone

Veículo

Placa (PK)

Modelo

Ano

Cor

Código do Cliente (FK)

Ordem de Serviço (OS)

Número (PK)

Data de Emissão

Data de Conclusão

Valor Total

Status

Serviço

Código (PK)

Descrição

Preço de Referência

Peça

Código (PK)

Nome

Preço

Equipe

Código (PK)

Nome da Equipe

Mecânico

Código (PK)

Nome

Endereço

Especialidade

Código da Equipe (FK)

Relacionamentos

Cliente - Veículo: Um cliente possui um ou mais veículos (1:N).

Veículo - Ordem de Serviço: Um veículo pode ter várias ordens de serviço (1:N).

Ordem de Serviço - Equipe: Uma ordem de serviço é atribuída a uma equipe (1:1).

Ordem de Serviço - Serviço: Uma ordem de serviço pode ter múltiplos serviços, e um serviço pode estar em várias ordens de serviço (N:N).

Ordem de Serviço - Peça: Uma ordem de serviço pode incluir várias peças, e uma peça pode ser usada em várias ordens de serviço (N:N).

Equipe - Mecânico: Uma equipe é composta por um ou mais mecânicos (1:N).

Modelo Conceitual

Um diagrama de entidade-relacionamento (DER) foi elaborado para ilustrar as entidades e seus relacionamentos. Utilize ferramentas como Draw.io ou dbdiagram.io para visualizá-lo.

Estrutura das Tabelas

Tabelas Intermediárias

OS_Serviço

Número da OS (FK)

Código do Serviço (FK)

Quantidade

Valor Total do Serviço

OS_Peça

Número da OS (FK)

Código da Peça (FK)

Quantidade

Valor Total das Peças

Como Utilizar Este Projeto

Clone este repositório em sua máquina local.

Use o esquema conceitual como base para criar o banco de dados relacional.

Implemente consultas SQL ou uma aplicação para gerenciar as ordens de serviço.

Decisões de Design

Cardinalidades: Baseadas no contexto real de uma oficina mecânica.

Tabelas Intermediárias: Criadas para representar os relacionamentos N:N entre Ordem de Serviço, Serviço e Peça.

Atributos: Escolhidos com base na narrativa para armazenar todas as informações necessárias.

Contribuições

Contribuições são bem-vindas! Caso tenha sugestões ou melhorias, abra uma issue ou envie um pull request.

Autor

Alisson Machado

