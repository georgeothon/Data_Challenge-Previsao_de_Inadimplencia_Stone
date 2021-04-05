# Case Data Science - Previsão de probabilidade de default (PD)

O Data Challenge é um desafio baseado em dados elaborado pelo time de dados da Stone.
Este repositório contém o [notebook](https://github.com/georgeothon/Data_Challenge-Previsao_de_Inadimplencia_Stone/blob/main/Data_Challenge_Stone.ipynb) e os arquivos referentes ao level 3 - O case, para o desafio de ciência de dados - Previsão de inadimplencia (Previsão de default).

## Descrição do problema

A stone é uma empresa que oferece crédito para empreendedores, no entando, o produto de crédito funciona de maneira diferente do mercado. Neste produto o cliente paga sua dívida com uma porcentagem das transações realizadas através das maquininhas de cartão que a própria Stone fornece, tanto de suas vendas físicas, quanto de suas vendas digitais.

E o desafio é estimar, no dia 90 do contrato, a probabilidade do cliente não quitar a dívida até o vencimento do contrato.

## Descrição dos dados

Os dados fornecidos são de pagamento, dívida, data do desembolso do empréstimo, entre outros, para cada dia de vigência do contrato, ou seja, após o desembolso, houve uma atualização diária na base incluindo novas informações sobre a dívida. Sendo assim, temos informações de clientes desde o dia desembolso até a data mais recente de informação de contrato, podendo ser do final do contato, ou até algum momento no tempo em que a data atual dos dados é menor que data final contrato.

Para uma abordagem por meio de métodos estatísticos e de machine learning, foi necessário agrupar esses dados por cliente criando novas variáveis de agregação, como algumas citadas abaixo:

- Porcentagem de pagamento do empréstimo.
- Valor médio da dívida total.
- Porcentam de dias de contrato sem pagamento.
- Entre outras...

Além disso, foram criadas variávies por intervalo de tempo dentro dos 90 dias, como variáveis agregadas para os primeiros 30 dias, para o intervalo entre o dia 30 e o dia 60 de contrato, além de alguns outros intervalos de tempo para as variáveis citadas de agregação criadas.

Por fim, como queremos estimar a probabilidade de default no dia 90 do contrato, para nossa análise, foi utilizada apenas dados com informação de no máximo 90 dias após o desembolso do crédito.

## Resultados

Obtivemos excelentes resultados para estimar a probabilidade de que o cliente não quite sua dívida. O desvio padrão do pagamento esperado em alguns intervalos de tempo não teve importância no modelo e foi retirado para diminuir a complexidade e que o modelo não degrade ao longo do tempo. Já a porcentagem de dias sem transação entre o dia 30 e o dia 90 do contrato, e a porcentagem de pagamento do empréstimo até o dia 90 do contrato foram variáveis que tiveram bastante importância para a classificação.

O modelo foi retreinado em todos os dados de teste recebidos para prever a probabilida de default nos dados de teste recebidos para avaliação, e os resultados serão atualizados assim que obtidos.


## Autor

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/georgeothon"><img src="https://avatars.githubusercontent.com/u/60243072?v=3?s=100" width="100px;" alt=""/><br /><sub><b>George Othon</b></td>
  </tr>
</table>
<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->
