# Modalidades de empréstimo

**Status: planejamento — implementação ainda não iniciada.**

Repositório de estudo de [José Carlos](https://github.com/carlos0ff), organizado a partir da [seleção de desafios de Matheus Leandro](https://www.matheusleandro.com.br/desafios).

## Objetivo

Criar uma API que receba dados de um cliente e informe as modalidades de crédito previstas pelas regras do exercício.

## Contrato previsto

`POST /customer-loans` recebe `age`, `cpf`, `name`, `income` e `location`. A resposta contém `customer` e `loans`; cada modalidade informa `type` e `interest_rate`.

| Modalidade | Taxa do exercício | Condição |
| --- | --- | --- |
| Pessoal — `PERSONAL` | 4% | Renda até R$ 3.000; ou entre R$ 3.000 e R$ 5.000, com idade inferior a 30 anos e residência em SP |
| Garantia — `GUARANTEED` | 3% | Mesmas condições da modalidade pessoal |
| Consignado — `CONSIGNMENT` | 2% | Renda a partir de R$ 5.000 |

## Pontos a documentar

O enunciado apresenta um exemplo de resposta que diverge das condições descritas. A implementação deverá registrar a interpretação adotada e o tratamento dos limites, especialmente R$ 5.000.

## Critérios de conclusão

- [ ] Implementar regras e contrato.
- [ ] Validar entradas.
- [ ] Testar renda nos limites, idade de 30 anos e localidades diferentes.
- [ ] Documentar respostas e execução.

## Tecnologia planejada

Java e Spring Boot. Versões, build e necessidade de persistência serão definidos durante o desenvolvimento.

## Como executar

Este repositório contém apenas a documentação inicial. Ainda não há aplicação, scripts de execução ou testes executáveis. Os comandos serão adicionados junto com a implementação.

## Referências e créditos

- [Enunciado na plataforma](https://www.matheusleandro.com.br/desafios/desafio-dos-emprestimos)
- [Referência original indicada pela plataforma](https://github.com/backend-br/desafios/blob/master/loans/PROBLEM.md)

Este README resume a proposta e registra um plano de trabalho. Os créditos do enunciado pertencem aos autores das referências; a solução será desenvolvida neste repositório.
