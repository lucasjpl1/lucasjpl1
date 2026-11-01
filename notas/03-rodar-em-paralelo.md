# Rodar em paralelo

<sub>Estoque · migração de ERP · gestão de mudança</sub>

## Contexto
O sistema de estoque antigo aceitava saldo negativo, e a produção dependia disso para conseguir emitir ordens de produção. O sistema novo tinha regras que bloqueiam esse tipo de movimentação por padrão.

## O que eu fiz
- Em vez de virar a chave de uma vez, decidimos manter os dois sistemas rodando em paralelo por um período de validação.
- Levei a dúvida ao fornecedor do sistema novo para entender se era possível replicar o comportamento e quais eram as consequências (custo, configuração, riscos).
- Separei o que é regra do sistema do que é hábito da operação, para decidir o que adaptar em cada lado.

## Resultado
A operação continuou sem parar enquanto as regras do estoque eram definidas, e a decisão final passou a se apoiar em teste real — não em suposição.

## O que eu levo disso
Quando a regra do sistema novo contradiz a operação, primeiro entenda **por que** a operação funciona daquele jeito. Às vezes quem precisa mudar é o processo; às vezes é a configuração.

---
[← todas as notas](./README.md)
