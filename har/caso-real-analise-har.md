# 🌐 Caso real: Análise de HAR em incidente de sistema web

## 🎯 Contexto do incidente

Durante a utilização de um sistema web corporativo, foi reportado comportamento de lentidão e falha intermitente no carregamento de determinadas funcionalidades.

Apesar de não haver erro explícito na aplicação, o usuário percebia demora significativa em requisições específicas.

---

## 🔍 Sintomas observados

- Lentidão em requisições específicas
- Carregamento parcial de dados na interface
- Diferença de tempo entre chamadas similares
- Ausência de erro explícito no backend

---

## 🧠 Primeira análise

Inicialmente, as hipóteses consideradas foram:

- problema de performance no backend
- sobrecarga na API
- lentidão no banco de dados
- instabilidade de rede
- comportamento intermitente do front-end

---

## 📦 Evidência principal: HAR file

A análise foi conduzida utilizando arquivo HAR (HTTP Archive), permitindo visualizar toda a cadeia de requisições HTTP realizadas pelo navegador.

---

## 🔎 O que foi analisado no HAR

- tempo de DNS lookup
- tempo de conexão TCP
- tempo de resposta do servidor (TTFB)
- tamanho das respostas
- status HTTP das requisições
- dependência entre chamadas

---

## ⚙️ Ponto crítico identificado

Foi identificado que algumas requisições:

- não apresentavam erro
- mas possuíam tempo de resposta elevado
- impactando diretamente o carregamento da interface

O gargalo não estava no erro, mas no tempo de resposta acumulado de chamadas sequenciais.

---

## 🧪 Interpretação técnica

O comportamento indicava:

- possível gargalo em API específica
- efeito cascata de requisições dependentes
- impacto de latência em chamadas sequenciais no front-end

---

## 📌 Conclusão técnica

A análise de HAR permitiu identificar que o problema não era uma falha funcional, mas sim um problema de performance perceptível na camada de integração entre front-end e backend.

---

## 🧠 Aprendizado

- nem todo problema web gera erro visível
- performance pode ser percebida como “bug”
- HAR é essencial para troubleshooting de aplicações web modernas
- análise de tempo de resposta é tão importante quanto análise de erro

---

## ⚙️ Nota

Este caso foi anonimizado e adaptado para fins de estudo técnico e documentação de troubleshooting.
