# Comandos SQL usando Pyhton + DuckDB

## Relacionamento com tabelas Cliente, ItensVenda, Produto, Venda

    Este Notebook mostra como importar a biblioteca DuckDB, ler arquivos CSV, relacioná-los com SQL.
    
	select CAST(v.data AS DATE)as data_venda, c.descricao as cliente, p.descricao, i.item_quantidade as qtd, v.valor_venda
    from db_venda v
    join db_cliente c ON (v.cliente_id = c.id)
    join db_itens_venda i ON (v.id = i.vendas_id)
    join db_produto p ON (i.produto_id = p.id)

