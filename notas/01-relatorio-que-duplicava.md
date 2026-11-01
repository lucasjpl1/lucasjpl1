# O relatório que duplicava vendas

<sub>SQL Server · relatórios · qualidade de dado</sub>

## Contexto
Um relatório de faturamento usado pela empresa mostrava totais acima do real. Nada quebrava, nenhum erro aparecia — o número só estava errado, o que é o tipo de problema mais perigoso, porque decisões continuam sendo tomadas em cima dele.

## O que eu fiz
- Tirei a consulta do relatório e rodei por partes, começando só pela tabela principal.
- A cada junção adicionada, comparei a quantidade de linhas antes e depois.
- Numa das junções a contagem saltou: a tabela relacionada tinha mais de um registro por chave, e cada venda passava a aparecer várias vezes (*fan-out*).
- Reescrevi a consulta agregando os dados da tabela relacionada **antes** de juntar, garantindo uma linha por chave.

## Resultado
Os totais voltaram a bater com a fonte, e a consulta ficou mais fácil de ler e de manter.

## O que eu levo disso
Antes de confiar num número, conte as linhas em cada etapa. Se uma junção pode trazer mais de um registro por chave, agregue primeiro e junte depois.

---
[← todas as notas](./README.md)
