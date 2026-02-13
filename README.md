# 📱 Super App de Inteligência Financeira (PF + PJ)

Plataforma modular de gestão financeira pessoal e empresarial, com evolução para modelo SaaS.

## Visão do Produto

O sistema combina:

- Gestão financeira **Pessoa Física (PF)**.
- Gestão financeira **Pessoa Jurídica (PJ)**.
- **Reservas inteligentes** (cofrinhos).
- Simuladores de **investimento** e **compra**.
- **Score de saúde financeira** com recomendações adaptativas.
- **Painel administrativo** com controle de planos, permissões e operação SaaS.

## Módulos Principais

1. Autenticação e Usuários
2. Perfil Evolutivo Inteligente
3. Módulo PF
4. Módulo PJ
5. Reservas Inteligentes
6. Simulador de Investimentos
7. Simulador de Compras
8. Saúde Financeira (Score)
9. Alertas Inteligentes
10. Módulo de Licitações (opcional)
11. Painel Administrativo
12. Sistema de Planos e Permissões

## Funcionalidades-Chave

### 1) Autenticação e Usuários

- Cadastro com e-mail/senha
- Login e recuperação de senha
- Edição de perfil e exclusão de conta
- Controle de plano: `Essencial`, `Empresário`, `Licitação Pro`
- Controle de status: `ativo`, `suspenso`

### 2) Perfil Evolutivo Inteligente

- Questionário inicial financeiro e investidor
- Pontuação dinâmica positiva e negativa
- Níveis automáticos (gestão financeira e investidor)
- Recalculo mensal de perfil
- Recomendações e alertas adaptativos conforme maturidade

### 3) Módulo PF

- Múltiplas contas bancárias e saldo consolidado
- Registro de receitas/despesas com categorias e subcategorias
- Recorrências, parcelamentos e projeção de fatura futura
- Planejamento anual, metas e comparativo mensal

### 4) Módulo PJ

- Cadastro de empresa e fornecedores
- Faturamento, despesas fixas/variáveis e impostos
- Pró-labore e distribuição de lucro
- Contratos, centros de custo e fluxo de caixa projetado
- Indicadores: margem, dependência de cliente, capital de giro

### 5) Reservas Inteligentes (Cofrinhos)

- Reserva por percentual, valor fixo, manual ou por meta
- Vinculação com contrato/licitação
- Separação automática ao receber receita
- Transferência entre reservas, limites e bloqueio opcional
- Histórico e relatórios por reserva

### 6) Simulador de Investimentos

Entrada:

- valor inicial
- aporte mensal
- prazo
- taxa estimada
- tipo de investimento

Saída:

- valor acumulado
- lucro total
- cenário comparativo
- recomendação por perfil
- alerta de liquidez

### 7) Simulador de Compras

Entrada:

- produto/serviço
- valor
- forma de pagamento
- parcelas e juros

Saída:

- custo real total
- impacto no fluxo de caixa, reserva e score
- classificação: segura / moderada / arriscada
- sugestão estratégica de pagamento

### 8) Saúde Financeira (0–100)

Score composto por:

- reserva de emergência
- endividamento
- liquidez
- uso de crédito
- diversificação de renda
- regularidade financeira
- relação PF x PJ

### 9) Alertas Inteligentes

- Vencimentos e excesso de gasto
- Queda de reserva e aumento de dívida
- Meta atingida
- Eventos de investimento (alta, queda, prazo, oportunidade)

### 10) Licitações (Opcional)

- Cadastro de editais e status
- Upload de documentos e validade
- Checklist e alertas
- Simulação de proposta e margem mínima
- Integração automática com financeiro PJ quando ganha

### 11) Painel Administrativo (Super Admin)

- Gestão de usuários e bloqueios
- Gestão de planos e granularidade de módulos
- Gestão financeira SaaS (assinaturas e inadimplência)
- Métricas: MRR, ARR, churn, módulos mais usados
- Gestão de conteúdos educacionais e campanhas

### 12) Planos e Permissões

Controle por:

- plano contratado
- módulo habilitado
- feature específica
- regras condicionais

## Arquitetura Recomendada (MVP → Escala)

### Camadas

- **Frontend**: Web App administrativo + App mobile
- **Backend API**: serviços modulares (domínio por contexto)
- **Banco relacional**: usuários, finanças, planos, auditoria
- **Fila/eventos**: alertas, recálculos mensais, rotinas automáticas
- **Observabilidade**: logs, métricas e trilha de auditoria

### Contextos de Domínio

- Identity (auth, usuários, perfis)
- Finance PF
- Finance PJ
- Reservas
- Simulações
- Score & Inteligência
- Licitações
- Billing & Plans
- Admin

## Roadmap sugerido

### Fase 1 — Fundação

- Autenticação completa
- Perfil evolutivo inicial
- Módulo PF essencial
- Cofrinhos básicos
- Score inicial

### Fase 2 — Expansão

- Módulo PJ
- Simuladores de compra/investimento
- Alertas inteligentes
- Painel admin inicial

### Fase 3 — SaaS Completo

- Planos, permissões e billing
- Métricas avançadas
- Licitações opcional
- Multiempresa e multiusuário

### Fase 4 — Escala

- Open Finance
- White Label
- API externa
- Governança avançada

## Critérios de sucesso

- Melhorar score médio dos usuários ao longo dos meses
- Reduzir inadimplência pessoal/empresarial
- Aumentar consistência de aportes em reservas
- Elevar retenção por recomendações personalizadas

## Próximos passos técnicos imediatos

1. Definir stack (frontend, backend, banco, mensageria)
2. Modelar entidades principais (usuário, transação, reserva, plano)
3. Implementar autenticação e RBAC por plano/permissão
4. Criar módulo PF com transações e visão consolidada
5. Publicar primeiro dashboard com score e alertas

---

Este repositório inicia como documentação-base do produto para orientar implementação incremental e evolução para SaaS.
