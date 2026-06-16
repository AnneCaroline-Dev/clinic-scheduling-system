# Documento
12 - BDD (Behavior Driven Development)

## Versão
1.0

## Autor
Anne Caroline

## Data
16/06/2026


## Objetivo

Este documento descreve os critérios de aceitação das User Stories do MVP utilizando a abordagem BDD (Behavior Driven Development).

Formato:

Dado que [contexto]

Quando [ação]

Então [resultado esperado]

---

# US01 - Realizar Login

## Cenário: Login realizado com sucesso

Dado que o paciente possui uma conta cadastrada

Quando informar e-mail e senha válidos

Então o sistema deve permitir o acesso à aplicação

E direcionar o usuário para a tela inicial.

---

## Cenário: Credenciais inválidas

Dado que o paciente informou dados incorretos

Quando tentar realizar login

Então o sistema deve exibir uma mensagem de erro

E impedir o acesso.

---

# US02 - Visualizar Médicos

## Cenário: Exibir lista de médicos

Dado que existem médicos cadastrados no sistema

Quando o paciente acessar a tela de médicos

Então o sistema deve exibir a lista de médicos disponíveis

E suas respectivas especialidades.

---

# US03 - Visualizar Horários Disponíveis

## Cenário: Exibir horários disponíveis

Dado que o paciente selecionou um médico

Quando acessar a agenda disponível

Então o sistema deve exibir os horários livres para agendamento.

---

## Cenário: Não existem horários disponíveis

Dado que não existem horários livres para o médico selecionado

Quando o paciente acessar a agenda

Então o sistema deve exibir uma mensagem informando indisponibilidade.

---

# US04 - Agendar Consulta

## Cenário: Agendamento realizado com sucesso

Dado que existe um horário disponível

E o paciente selecionou um médico

Quando confirmar o agendamento

Então o sistema deve criar a consulta

E exibir uma mensagem de sucesso.

---

## Cenário: Horário indisponível

Dado que o horário foi ocupado por outro paciente

Quando o usuário tentar confirmar o agendamento

Então o sistema deve impedir a operação

E exibir uma mensagem de indisponibilidade.

---

# US05 - Visualizar Consultas Agendadas

## Cenário: Exibir consultas agendadas

Dado que o paciente possui consultas cadastradas

Quando acessar a área "Minhas Consultas"

Então o sistema deve exibir a lista de consultas agendadas.

---

## Cenário: Nenhuma consulta encontrada

Dado que o paciente não possui consultas agendadas

Quando acessar a área "Minhas Consultas"

Então o sistema deve exibir uma mensagem informando que não existem consultas cadastradas.

---

# US06 - Cancelar Consulta

## Cenário: Cancelamento realizado com sucesso

Dado que existe uma consulta agendada

Quando o paciente solicitar o cancelamento

E confirmar a operação

Então o sistema deve cancelar a consulta

E exibir uma mensagem de sucesso.

---

## Cenário: Cancelamento cancelado pelo usuário

Dado que existe uma consulta agendada

Quando o paciente iniciar o cancelamento

E desistir da operação

Então o sistema deve manter a consulta ativa.

---

# US07 - Reagendar Consulta

## Cenário: Reagendamento realizado com sucesso

Dado que existe uma consulta agendada

E existe um novo horário disponível

Quando o paciente selecionar o novo horário

E confirmar a alteração

Então o sistema deve atualizar a consulta

E exibir uma mensagem de sucesso.

---

## Cenário: Novo horário indisponível

Dado que o horário selecionado não está disponível

Quando o paciente tentar concluir o reagendamento

Então o sistema deve impedir a alteração

E exibir uma mensagem de erro.

---

# US08 - Receber Confirmação de Agendamento

## Cenário: Exibir confirmação após agendamento

Dado que o agendamento foi realizado com sucesso

Quando a operação for concluída

Então o sistema deve exibir uma mensagem de confirmação ao paciente.

---

# US09 - Receber Mensagens de Erro

## Cenário: Exibir mensagem de erro

Dado que ocorreu uma falha durante uma operação

Quando o sistema identificar o erro

Então deve exibir uma mensagem clara

Informando ao usuário o motivo da falha.

---

# Rastreabilidade

| User Story | Cenários BDD               |
| ---------- | -------------------------- |
| US01       | Login                      |
| US02       | Visualizar Médicos         |
| US03       | Visualizar Horários        |
| US04       | Agendar Consulta           |
| US05       | Visualizar Consultas       |
| US06       | Cancelar Consulta          |
| US07       | Reagendar Consulta         |
| US08       | Confirmação de Agendamento |
| US09       | Mensagens de Erro          |

---

# Benefícios

A utilização de BDD permite:

* Melhor alinhamento entre negócio e desenvolvimento;
* Critérios de aceitação claros;
* Redução de ambiguidades;
* Facilidade na criação de casos de teste;
* Maior qualidade na entrega do produto.
