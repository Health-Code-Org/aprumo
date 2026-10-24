<p align="center">
  <img src="./materiais-originais/joao-identidade-visual/logo-aprumo-gradiente.png" alt="Logo Aprumo" width="420">
</p>

<h1 align="center">Aprumo — Ergonomia e Postura</h1>

<p align="center">
  Monitor de postura com Arduino que alerta o usuário, em tempo real, quando ele permanece muito próximo da tela por tempo prolongado — um indicador direto de postura inadequada — na bancada de estudo ou trabalho.
</p>

---

## Sumário

- [Sobre o projeto](#sobre-o-projeto)
- [1. O problema](#1-o-problema)
- [2. A solução](#2-a-solução)
- [3. Identidade visual](#3-identidade-visual)
- [4. Pitch](#4-pitch)
- [5. Equipe e divisão de tarefas — Checkpoint 1](#5-equipe-e-divisão-de-tarefas-checkpoint-1)
- [6. Status do Checkpoint 1 · 19/10 a 23/10](#6-status-do-checkpoint-1-1910-a-2310)

---

## Sobre o projeto

Nosso projeto se chama **Aprumo**, um monitor de postura desenvolvido para ajudar a prevenir problemas de saúde causados pela má postura durante longos períodos sentados, seja estudando ou trabalhando. Muitas pessoas, principalmente estudantes e profissionais que passam horas em frente ao computador, acabam ficando curvadas e podem desenvolver dores nas costas e no pescoço.

Pensando nisso, nossa proposta é desenvolver um sistema que une **software de gerenciamento** a um **Arduino equipado com sensores**, capaz de identificar quando a pessoa permanece muito próxima da tela por um período prolongado (ex: 5 minutos) — sinal direto de que a postura está inadequada. Quando isso acontecer, o sistema emite um alerta luminoso e sonoro para lembrá-la de corrigir a postura. Nosso objetivo é incentivar hábitos mais saudáveis, promover o bem-estar e ajudar na prevenção de problemas relacionados à postura.

## 1. O problema

Passar muitas horas sentado, em má postura, estudando ou programando, está associado a dores lombares e cervicais e a lesões por esforço repetitivo (LER/DORT). O problema é silencioso: a pessoa raramente percebe quando a postura piora, e a dor só aparece depois, quando o dano já está instalado.

A dimensão do problema é expressiva. Segundo a PNS 2019, do IBGE, cerca de 21,6% dos adultos brasileiros (34,3 milhões de pessoas) relataram problema crônico de coluna. No mundo do trabalho, dados preliminares do INSS indicam que, em 2017, ao menos 22.029 trabalhadores ficaram mais de 15 dias afastados por LER/DORT, o equivalente a 11,19% dos benefícios concedidos por adoecimento no trabalho naquele ano.

O projeto foca em um recorte específico: a postura durante o uso prolongado do computador em mesas de estudo e de trabalho, e a falta de um aviso em tempo real que ajude a corrigi-la antes que a dor se instale.

**Público-alvo:** estudantes, profissionais de escritório e de tecnologia, e pessoas em home office. O contexto é a mesa de estudo ou de trabalho, em casa, em universidades e em escritórios, onde se passa grande parte do dia sentado diante do computador.

**Bases de dados públicas:**

- **IBGE, [Pesquisa Nacional de Saúde (PNS)](https://www.ibge.gov.br/estatisticas/sociais/saude/9160-pesquisa-nacional-de-saude):** prevalência de problema crônico de coluna na população adulta, usada para dimensionar o problema e justificar o público.
- **Ministério da Saúde, [SINAN/DATASUS](https://datasus.saude.gov.br/informacoes-de-saude-tabnet/):** notificações de agravos relacionados ao trabalho, incluindo LER/DORT; fonte de consulta para aprofundar a análise da ocorrência de lesões ligadas à postura e ao esforço repetitivo.
- **[Observatório de Segurança e Saúde no Trabalho (SmartLab)](https://observatoriosst.mpt.mp.br):** dados sobre afastamentos e doenças do trabalho, incluindo as osteomusculares; fonte de consulta para aprofundar o impacto no mundo do trabalho.
- **Previdência Social (INSS), [dados abertos](https://dadosabertos.inss.gov.br):** benefícios concedidos por doenças do sistema osteomuscular, usados para mostrar o custo social e econômico do problema.

📎 Material original: [`materiais-originais/sabrina-descricao-problema/`](./materiais-originais/sabrina-descricao-problema/)

## 2. A solução

Para enfrentar esse problema, o Aprumo combina um sensor de distância — que monitora a aproximação da pessoa em relação à tela — com um software de gerenciamento que registra esses dados ao longo do tempo. Quando a pessoa permanece muito próxima da tela por tempo prolongado, o sistema emite alertas de luz e som para incentivar a correção da postura antes que surjam dores, enquanto o histórico registrado ajuda a acompanhar os hábitos e a estimular pausas durante o dia.

**Componentes essenciais:**
- Arduino Uno R3 ou Nano V3
- Sensor de distância: HC-SR04 (ultrassônico) ou VL53L0X (laser ToF)
- LED RGB com resistores
- Buzzer de 5V
- Cabo USB
- Protoboard e jumpers

**Componentes opcionais:**
- Botão para calibração
- Display OLED para exibir informações
- Sensor MPU-6050 para identificar inclinações
- Caixa de proteção para organizar os componentes

**Por que essas escolhas:** o Arduino e os sensores foram escolhidos pelo baixo custo e pela facilidade de montagem. O sensor de distância identifica quando a pessoa está muito próxima da tela, enquanto o LED e o buzzer emitem alertas para corrigir a postura. A protoboard e os jumpers facilitam as conexões e os testes. Já os componentes opcionais permitem aprimorar o projeto, adicionando informações visuais e uma análise mais completa da inclinação corporal.

📎 Material original: [`materiais-originais/dyovanna-proposta-solucao/`](./materiais-originais/dyovanna-proposta-solucao/)

## 3. Identidade visual

<p align="center">
  <img src="./materiais-originais/joao-identidade-visual/logo-aprumo-gradiente.png" alt="Logo Aprumo" width="280">
</p>

**Paleta de cores**

| Cor | Hex | Uso |
|---|---|---|
| Verde Menta | `#34D399` | Marca — detalhes, gradiente do logo |
| Verde Aprumo | `#10B981` | Marca — cor principal / wordmark |
| Azul Vibrante | `#2563EB` | Marca — destaques, cor secundária |
| Azul Profundo | `#0F2C59` | Marca — texto "aprumo", títulos |

**Cores de status da aplicação** (usadas na interface/alertas do sistema — não na marca):

| Status | Hex | Significado |
|---|---|---|
| Postura OK | `#10B981` | Coluna alinhada |
| Atenção | `#F59E0B` | Início de curvatura |
| Correção | `#EF4444` | Postura incorreta |

**Tipografia oficial**

| Uso | Fonte |
|---|---|
| Logotipo | Garet Bold |
| Títulos | Inter SemiBold |
| Texto geral | Inter Regular |

📎 Material original: [`materiais-originais/joao-identidade-visual/`](./materiais-originais/joao-identidade-visual/)

## 4. Pitch

O Aprumo é um monitor de postura com Arduino e sensor de distância: ele percebe quando a pessoa fica perto demais da tela por tempo prolongado e, nesse momento, avisa com luz e som para que ela se corrija — incentivando hábitos mais saudáveis e ajudando a prevenir dores relacionadas à má postura.

📎 Material original: [`materiais-originais/leandro-pitch-inicial/`](./materiais-originais/leandro-pitch-inicial/)

## 5. Equipe e divisão de tarefas — Checkpoint 1

| Integrante | Entrega | Status |
|---|---|---|
| Sabrina | Descrição do problema | ✅ Concluído |
| Dyovanna | Proposta de solução tecnológica | ✅ Concluído |
| João | Identidade visual | ✅ Concluído |
| Leandro | Pitch inicial | ✅ Concluído |
| Nicolas | Junção e centralização no repositório GitHub | ✅ Concluído |

## 6. Status do Checkpoint 1 · 19/10 a 23/10

- [x] Descrição do problema
- [x] Proposta de solução tecnológica
- [x] Identidade visual
- [x] Pitch inicial
- [x] Repositório público, organizado, com participação de todos os integrantes
