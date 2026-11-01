# Auditar antes de migrar

<sub>Migração de ERP · master data · SQL Server · Next.js</sub>

## Contexto
A empresa ia migrar do ERP legado para um sistema novo. O cadastro de produtos estava espalhado em cinco bancos — um central e um por filial — e a expectativa era simplesmente exportar e importar.

## O que eu fiz
- Cruzei os cadastros dos cinco bancos procurando o mesmo código com significados diferentes, itens que só existiam em uma filial e registros sem vínculo.
- Os números foram altos o suficiente para bloquear a migração: mais de mil conflitos de código e milhares de registros órfãos.
- Montei um dossiê para a diretoria explicando o que cada problema causaria no sistema novo se fosse migrado como estava.
- Transformei as consultas da auditoria numa ferramenta interna (Next.js), com abas por tipo de problema, para acompanhar a limpeza de forma contínua.

## Resultado
A migração passou a ter uma etapa explícita de saneamento, com acompanhamento visível para todos — em vez de descobrir os problemas depois da virada.

## O que eu levo disso
Migração não é cópia de dados, é decisão sobre eles. Dado sujo migrado continua sujo — só que num sistema novo, onde ninguém espera encontrá-lo.

---
[← todas as notas](./README.md)
