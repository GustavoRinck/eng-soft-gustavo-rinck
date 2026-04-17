# Documento de Requisitos de Software (SRS) #

## Informações do Projeto ##


| Campo   |      Descrição      |
|----------|:-------------:|
| Nome do Projeto: |  Sistema de Gestão Hoteleira Bela Vista | 
| Dono do Projeto: |    Hotel Bela Vista   |  
| Versão: | 1.0|
| Data: | 16/04/2026 | 




## 1. Introdução ##
O objetivo deste documento é descrever os requisitos para o desenvolvimento de um sistema de gestão para o Hotel Bela Vista. O sistema tem como finalidade organizar as reservas, evitar conflitos de quartos, controlar consumo de hóspedes, gerenciar estoque e auxiliar nas operações do hotel, substituindo processos manuais atualmente realizados em papel.

## 2. Escopo ##
O sistema abrangerá as seguintes funcionalidades principais:

* Funcionalidade 1: Gestão de reservas e controle de ocupação dos quartos

* Funcionalidade 2: Controle de hóspedes, consumo (recepção e frigobar) e faturamento

* Funcionalidade 3: Gestão de estoque, limpeza e operações internas

* Funcionalidade 4: Relatórios gerenciais e histórico de hóspedes

## 3. Requisitos Funcionais ##
### 3.1 Gestão de Reservas e Quartos ###

* RF 1.1:
O sistema deve impedir o registro de reservas para quartos já ocupados no mesmo período.

* RF 1.2:
O sistema deve avisar imediatamente quando houver tentativa de reserva conflitante.

* RF 1.3:
O sistema deve apresentar um mapa visual de quartos com status por cores (livre, ocupado, sujo).

* RF 1.4:
O sistema deve diferenciar automaticamente os preços conforme o tipo de quarto (simples, luxo, família).


### 3.2 Cadastro de Hóspedes e Histórico ###

* RF 2.1:
O sistema deve permitir cadastro de hóspedes com nome, CPF e telefone.

* RF 2.2:
O sistema deve recuperar automaticamente dados de hóspedes já cadastrados via CPF.

* RF 2.3:
O sistema deve manter histórico de hospedagens e preferências dos clientes.

* RF 2.4:
O sistema deve armazenar os dados dos hóspedes por até 1 ano.


### 3.3 Consumo e Faturamento ###

* RF 3.1:
O sistema deve registrar consumo de itens na conta do hóspede (recepção, frigobar e serviços).

* RF 3.2:
O sistema deve permitir lançamento rápido de consumo por seleção de itens (sem necessidade de digitar preço).

* RF 3.3:
O sistema deve calcular automaticamente o total da conta no checkout (diárias + consumos).

* RF 3.4:
O sistema deve permitir cobrança de serviços extras (lavanderia, café extra, danos).


### 3.4 Frigobar e Estoque ###

* RF 4.1:
O sistema deve permitir cadastro de produtos (água, refrigerante, chocolate, etc.) com preços editáveis.

* RF 4.2:
O sistema deve permitir definir diferentes configurações de frigobar por tipo de quarto.

* RF 4.3:
O sistema deve registrar consumo do frigobar por quarto.

* RF 4.4:
O sistema deve atualizar automaticamente o estoque ao registrar consumo ou reposição.

* RF 4.5:
O sistema deve permitir entrada manual de estoque por quantidade (ex: “50 águas”).

* RF 4.6:
O sistema deve avisar quando houver necessidade de reposição de itens no estoque ou nos quartos.


### 3.5 Limpeza e Status dos Quartos ###

* RF 5.1:
O sistema deve permitir marcar quartos como “precisando de limpeza”.

* RF 5.2:
O sistema deve automaticamente marcar o quarto como “sujo” ao finalizar uma reserva.

* RF 5.3:
O sistema deve permitir solicitação de limpeza manual pelo recepcionista.

* RF 5.4:
O sistema deve notificar a equipe de limpeza sobre quartos pendentes.


### 3.6 Controle de Acesso ###

* RF 6.1:
O sistema deve restringir acesso apenas a funcionários autorizados.


### 3.7 Relatórios ###

* RF 7.1:
O sistema deve gerar relatório mensal de faturamento.

* RF 7.2:
O relatório deve apresentar ganhos com diárias e consumos separados.

* RF 7.3:
O sistema deve informar quantidade de hóspedes atendidos no período.


## 4. Requisitos Não Funcionais ##

* RNF 4.1: (Mobilidade): O sistema deve funcionar em computadores, tablets e celulares.

* RNF 4.2: (Usabilidade): Interface simples, com linguagem clara e uso de cores para facilitar a operação.

* RNF 4.3: (Desempenho): O sistema deve responder em até 2 segundos.

* RNF 4.4: (Segurança): Acesso via login e senha para funcionários.

* RNF 4.5: (Disponibilidade): Disponibilidade mínima de 99%.

## 5. Design da Interface do Usuário (UI) ##

Design 1: Mapa de quartos com cores:

* Verde: livre

* Vermelho: ocupado

* Amarelo: sujo

Design 2: Navegação simples com botões diretos:

* Reservar quarto

* Lançar consumo

* Ver mapa

* Fechar conta

## 6. Arquitetura do Sistema ##

Arquitetura: Sistema web em arquitetura em camadas

Tecnologias sugeridas:
* Backend: Node.js

* Frontend: HTML, CSS

* Banco de Dados: PostgreSQL

## 7. Requisitos de Dados ##

Entidades principais:

* Hóspedes;

* Quartos;

* Reservas;

* Consumo;

* Produtos;

* Estoque;

* Funcionários;

Regras:

* Integridade entre reservas e quartos;

* Atualização automática de estoque;

* Backup periódico;

## 8. Requisitos de Segurança ##

* Autenticação com login e senha;

* Controle de acesso por tipo de funcionário;

* Uso de HTTPS e proteção de dados sensíveis;

## 9. Requisitos de Desempenho ##

* Suporte a múltiplos usuários simultâneos;

* Baixo tempo de resposta (até 2 segundos);

## 10. Requisitos de Teste ##

* Testes unitários e de integração;

* Testes de aceitação com cenário real (reservas, consumo, limpeza);


## 11. Cronograma do Projeto ##


| Tarefa   |      Data de Início      |  Data de Término |
|----------|:-------------:|------:|
| Levantamento de Requisitos |  7/04/2026 | 16/04/2026 |
| Design |    xx/xx/xxxx   |     xx/xx/xxxx  |
| Desenvolvimento |  xx/xx/xxxx  |     xx/xx/xxxx  |
| Testes |  xx/xx/xxxx  |     xx/xx/xxxx  |
| Implantação |  xx/xx/xxxx  |     xx/xx/xxxx  |





## Revisões ##

| Versão   |      Data      |  Descrição |
|----------|:-------------:|------:|
| 1.0 |  16/04/2026 |  Versão inicial baseada na entrevista com o cliente|












