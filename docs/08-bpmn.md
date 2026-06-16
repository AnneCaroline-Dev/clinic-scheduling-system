# Documento
08 - bpmn
## Versão
1.0

## Autor
Anne Caroline

## Data
16/06/2026


Início

↓

Selecionar Médico

↓

Selecionar Horário

↓

Horário Disponível?

├── Não → Exibir Mensagem

└── Sim → Confirmar Agendamento

↓

Criar Consulta

↓

Fim

------------------------------------------------

# Processo de Cancelamento

Início

↓

Selecionar Consulta

↓

Solicitar Cancelamento

↓

Confirmar?

├── Não → Retornar

└── Sim → Cancelar Consulta

↓

Fim

------------------------------------------------

# Processo de Reagendamento

Início

↓

Selecionar Consulta

↓

Escolher Novo Horário

↓

Horário Disponível?

├── Não → Exibir Mensagem

└── Sim → Atualizar Consulta

↓

Fim