# 🧠 Caso real: Incidente em Agenda Integrada (ERP Hospitalar)

## 🎯 Contexto do incidente

Durante a utilização da Agenda Integrada em um ambiente corporativo hospitalar, foi identificado um comportamento inconsistente na geração e exibição de horários disponíveis para agendamento.

O sistema apresentava divergência entre a disponibilidade esperada e os horários efetivamente sugeridos.

---

## 🔍 Sintomas observados

- Horários disponíveis não eram exibidos corretamente
- Sugestões de agenda inconsistentes entre profissionais e especialidades
- Falhas intermitentes na geração de horários
- Diferença entre regras configuradas e resultado apresentado

---

## 🧠 Primeira análise

Inicialmente, o comportamento sugeria possíveis causas como:

- falha na regra de negócio de agenda
- inconsistência na ordem de processamento de itens
- indisponibilidade de recursos vinculados ao profissional
- conflito entre agendas associadas

---

## 🔎 Hipóteses levantadas

Foram consideradas as seguintes hipóteses:

- Problema na regra de prioridade entre itens de agenda
- Conflito entre agendas vinculadas ao profissional
- Restrição de disponibilidade baseada em recursos ou especialidades
- Ordem de processamento impactando sugestão de horários
- Limitação no motor de sugestão de horários (Smart Schedule)

---

## 🧪 Processo de investigação

A análise foi conduzida com base em:

- validação das regras de configuração da agenda
- análise de relacionamento entre profissionais e agendas
- verificação de ordem de itens na geração de sugestões
- comparação entre horários esperados vs retornados
- revisão de comportamento do motor de sugestão (Smart Schedule)

---

## ⚙️ Resultado da análise

O comportamento foi associado à forma como o sistema processa a disponibilidade dos itens de agenda, considerando regras de prioridade e dependências entre recursos vinculados.

Foi identificado que o resultado da sugestão pode variar conforme a combinação de regras aplicadas e a ordem de avaliação dos itens configurados.

---

## 📌 Conclusão técnica

Este tipo de incidente reforça que:

> Em sistemas de agenda complexos, o problema nem sempre está na disponibilidade em si, mas na forma como as regras de negócio são avaliadas e combinadas pelo motor de sugestão.

---

## 🧠 Aprendizados

- Regras de agenda têm comportamento dependente de ordem e prioridade
- A sugestão de horários não é apenas “consulta de disponibilidade”
- Pequenas alterações em configuração podem alterar completamente o resultado
- É essencial validar regras antes de assumir defeito funcional

---

## ⚙️ Nota

Este caso foi anonimizado e adaptado para fins de estudo técnico e documentação de troubleshooting.
