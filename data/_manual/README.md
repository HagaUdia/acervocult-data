# Carga manual

Lista de obras obtida fora do scraping — planilha de pedido institucional
(LAI/Fala.BR, e-SIC) ou lista enviada pela própria plataforma.

Grave o arquivo como `<streaming>.csv` ou `<streaming>.json` nesta pasta, usando
o mesmo `id` do streaming (`telabrasil`, `oldflix`…). A cada
coleta o conteúdo entra **somando** ao que os coletores trouxerem, e vale a
mesma regra mínima: nome + (ano ou diretor).

## CSV

Cabeçalho com as colunas que existirem, em qualquer ordem. Aceita também os
nomes em português (`titulo`, `ano`, `direcao`):

```csv
name,year,director,url
Ilha das Flores,1989,Jorge Furtado,https://telabrasil.cultura.gov.br/obra/ilha-das-flores
Bacurau,2019,Kleber Mendonça Filho,
```

## JSON

```json
[
  { "name": "Ilha das Flores", "year": 1989, "director": "Jorge Furtado" }
]
```

## De onde vem cada carga

- **Tela Brasil** — pedido pelo Fala.BR (LAI) ao Ministério da Cultura, pedindo
  "a relação completa de obras da plataforma Tela Brasil, com título, ano e
  tipo". Prazo legal de 20 dias. Vale checar antes o dados.gov.br.
- **Oldflix** — o catálogo está sob `Disallow` no robots.txt; se a plataforma
  responder ao pedido por e-mail com a lista, ela entra por aqui.
