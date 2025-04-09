# 📘 Padrões de Projeto no Sistema de Logística

## 🔍 Strategy

**Objetivo**: Permitir cálculo dinâmico de fretes para diferentes modalidades (Expressa, Econômica, Terceirizada).

**Implementação**:
- Interface `FreteStrategy` com método `calcularFrete()`
- Classes concretas para cada modalidade (`EntregaExpressa`, `EntregaEconomica`)

**Vantagem**: Adicionar novas modalidades sem alterar código existente.

## 🔌 Adapter

**Objetivo**: Integrar API externa de transportadora com interface incompatível.

**Implementação**:
- `TransportadoraAdapter` adapta a `APITransportadoraExterna` para o sistema
- Implementa a interface `TransportadoraTerceirizada`

**Vantagem**: Isolar detalhes da API externa, mantendo o sistema desacoplado.