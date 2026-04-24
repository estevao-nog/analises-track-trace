# 📊 Análise de Impacto T&T - Dashboards Interativos

Visualizações interativas das associações do sistema Track & Trace com foco em impacto de bloqueio.

## 📁 Arquivos

### 🎯 **dashboard.html** - Dashboard Principal
- **O quê**: KPIs, gráficos de distribuição, análise de status
- **Como abrir**: Clique duplo ou abra no navegador
- **Principais visualizações**:
  - Total de viagens: 40.863
  - Distribuição por Checkin Source (Motora, SAP, Workstation, GUIA)
  - Impacto de bloqueio: 38.88% das viagens
  - Comparação: Linhas vs Viagens (metodologia corrigida)
  - Status de todas as viagens
  - Status detalhado das viagens bloqueadas via SAP

### 🌳 **tree-interactive.html** - Árvore Hierárquica Interativa
- **O quê**: Visualização sunburst mostrando hierarquia completa
- **Hierarquia**: Total → Status → Checkin Source
- **Como usar**:
  - Clique em um segmento para expandir
  - Hover para ver valores exatos
  - Clique no centro para voltar um nível
- **Cores por Status**:
  - 🟢 Verde: Concluído (18.528 viagens - 45.33%)
  - 🔴 Vermelho: Fechadas (14.291 viagens - 34.96%)
  - 🟠 Laranja: Cancelado (4.469 viagens - 10.93%)
  - 🔵 Azul: Pendente (3.152 viagens - 7.71%)

## 🔗 Links Compartilháveis

### Opção 1: GitHub Pages (recomendado)
```
https://estevao-nog.github.io/analises-track-trace/dashboard.html
https://estevao-nog.github.io/analises-track-trace/tree-interactive.html
```

### Opção 2: jsDelivr (alternativa rápida)
```
https://cdn.jsdelivr.net/gh/estevao-nog/analises-track-trace@main/dashboard.html
https://cdn.jsdelivr.net/gh/estevao-nog/analises-track-trace@main/tree-interactive.html
```

## 📊 Base de Dados

- **Total de Viagens**: 40.863
- **DocumentType**: 6 (Operações apenas)
- **Período**: 03 a 23 de Abril/2026
- **Metodologia**: Contagem por DocumentNumber Distinto (viagens, não linhas)

## 🎯 Status das Viagens

| Status | Nome | Viagens | % |
|--------|------|---------|---|
| 1 | Concluído | 18.528 | 45.33% |
| 4 | Fechadas | 14.291 | 34.96% |
| 3 | Cancelado | 4.469 | 10.93% |
| 2 | Pendente | 3.152 | 7.71% |
| - | Sem Status | 423 | 1.04% |

## 📍 Checkin Source (Fontes)

| Código | Nome | Tipo | Descrição |
|--------|------|------|-----------|
| 3 | Motora | T&T | App móvel do motorista |
| 4 | SAP | Contingência | Sistema SAP (sem T&T) |
| 5 | Workstation | T&T | Estação de trabalho |
| 10 | Tracking | GPS | Rastreamento GPS |
| 11 | GUIA | T&T | Sistema GUIA |

## ⚡ Impacto de Bloqueio

Se bloquear entrada sem T&T (apenas SAP):
- **Viagens bloqueadas**: 15.888 (38.88%)
- **Viagens mantidas**: 24.975 (61.12%)
- **Risco**: 🟡 MODERADO (com bloqueio gradual)

### Status das Bloqueadas:
- ✅ Com sucesso: 7.919 (49.84%) - operações que funcionaram
- 🔴 Com erro: 6.297 (39.63%) - com problemas prévios
- ⚠️ Outras: 1.672 (10.52%) - casos especiais

## 🎬 Recomendação

**Implementar bloqueio gradual em 3 fases (4-6 semanas)**:

1. **Fase 1 (Dias 1-14)**: Comunicação - 0% impacto
2. **Fase 2 (Dias 15-28)**: Endurecimento - 15-20% impacto
3. **Fase 3 (Dias 29+)**: Bloqueio total - 38.88% impacto (após >80% adesão)

## 📱 Compatibilidade

- ✅ Desktop (Chrome, Firefox, Edge, Safari)
- ✅ Tablet (responsivo)
- ✅ Mobile (responsivo)
- ✅ Sem requisitos de servidor ou instalação

## 📞 Suporte Técnico

- **Dúvidas sobre dados**: Consulte RELATORIO_CORRIGIDO_QUESTOES_PRINCIPAIS.md
- **Dúvidas sobre metodologia**: Consulte EXPLICACAO_METODOLOGIA_CORRIGIDA.md
- **Como usar o dashboard**: Consulte GUIA_DASHBOARD.md

---

**Versão**: 2026-04-24  
**Autor**: Análise de Impacto T&T  
**Status**: ✅ Pronto para Apresentação
