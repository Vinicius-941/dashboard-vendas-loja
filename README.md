# Dashboard de vendas de uma loja fictícia

Projeto de portfólio de análise de dados: dados brutos → tratamento com Python/Pandas → dashboard no Power BI.

## Estado atual

O repositório contém apenas a base bruta e a documentação inicial. O script de tratamento, os dados tratados e o dashboard ainda serão desenvolvidos pelo autor.

## Base de dados

Arquivo: `data/raw/vendas_brutas.xlsx`, aba `vendas_brutas`.

Todos os dados são **simulados**, criados para fins educacionais. Não representam uma empresa ou clientes reais.

- Loja fictícia de tecnologia, com 10 produtos e três canais de venda.
- Período: janeiro a dezembro de 2025.
- 2.440 registros: 2.400 vendas simuladas e 40 cópias exatas de registros.
- Uma linha representa a venda de um único produto. A quantidade pode ser maior que uma unidade.
- Os identificadores de clientes são fictícios.
- A base contém inconsistências intencionais, como campos vazios, espaços extras, variações de grafia, datas em formatos diferentes e valores monetários misturados entre números e texto.
- Não há fórmulas, totais, indicadores ou tratamento na planilha. Não há metas de vendas nesta versão.

## Dicionário de dados

| Coluna | Significado |
|---|---|
| id_venda | Identificador da venda; pode aparecer novamente por duplicação da exportação |
| data_venda | Data da venda em 2025 |
| id_cliente | Identificador fictício do cliente |
| id_produto | Código do produto |
| produto | Nome do produto |
| categoria | Categoria do produto |
| quantidade | Número de unidades vendidas |
| preco_unitario | Preço unitário antes do desconto, em reais |
| custo_unitario | Custo unitário do produto, em reais |
| desconto_percentual | Desconto em pontos percentuais: 10 significa 10%; vazio significa informação ausente |
| canal | Canal de venda |
| cidade | Cidade da venda |
| uf | Unidade federativa |
| forma_pagamento | Forma de pagamento |
| status | Concluída, Cancelada ou Devolvida |

## Perguntas para a análise

- Como as vendas evoluem ao longo dos meses?
- Quais produtos e categorias geram mais receita e lucro bruto?
- Como os canais de venda se comparam?
- Qual é o ticket médio das vendas concluídas?
- Como os descontos se relacionam com o resultado das vendas?
- Qual é a participação de cancelamentos e devoluções?

## Próximas etapas

1. Inspecionar a base e documentar os problemas de qualidade.
2. Desenvolver um script em Pandas, preservando o arquivo bruto.
3. Definir e documentar as regras para duplicatas, ausências e status das vendas.
4. Exportar os dados tratados para uma pasta `data/processed/`.
5. Importar o resultado no Power BI, definir as medidas e construir o dashboard.
6. Adicionar capturas do dashboard e conclusões ao README.

O lucro disponível para calcular é **bruto**: a base não contém impostos, frete, taxas ou despesas operacionais. As conclusões descrevem somente uma simulação. A base usa dias de 1 a 28 e não permite estudar fielmente efeitos de calendário.
