# Porsche Sales Overview — Dashboard DIO

Dashboard comercial interativo, responsivo e publicado como site estático pelo GitHub Pages. Foi construído em um único arquivo HTML, com CSS e JavaScript incorporados e sem dependências externas.

## Perguntas de negócio

1. **Quais modelos concentram o maior valor comercial registrado?** O gráfico ordena os dez modelos com maior soma de preços, ajudando a comparar a contribuição de cada modelo para o valor registrado.
2. **Quais formas de pagamento aparecem com maior frequência?** O gráfico de volume permite observar a composição dos pagamentos e apoiar discussões sobre experiência de compra e processos financeiros.
3. **Em quais cidades há maior concentração de registros?** O ranking das dez cidades com mais registros pode orientar investigações comerciais e a priorização de análises regionais.

## Indicadores e filtros

- KPIs: quantidade de registros filtrados, valor total registrado, ticket médio e quantidade/percentual com status `Delivered`.
- Filtros: modelo Porsche, ano do veículo, cidade e forma de pagamento.
- Os gráficos e indicadores são atualizados de acordo com os filtros selecionados.

## Tratamento dos dados

- Utilizei exclusivamente os campos sanitizados da aba `Sanitized` da planilha fornecida no desafio.
- Converti ano e preço para valores numéricos durante a preparação dos dados.
- O dashboard não incorpora nome de cliente, vendedor, ID da venda nem os campos originais não sanitizados.
- A planilha contém 100 registros, dos quais 24 têm data de venda classificada como `INVALID`. Por esse motivo, não foi criada uma série temporal de vendas: ela poderia sugerir uma evolução incompleta ou enganosa.
- O valor total é descrito como **valor registrado**, não como receita líquida ou receita realizada. Ele soma os preços de todos os registros, inclusive os que têm status `Cancelled`. O indicador de entregas considera apenas `Delivered`.
- A base apresenta 100 registros; resultados e rankings refletem os dados disponíveis, não necessariamente o universo completo de vendas Porsche.

## Prompt utilizado e iteração

Prompt inicial (adaptado para este projeto):

> Crie um dashboard comercial interativo de vendas Porsche em um único arquivo `index.html`, usando apenas os campos sanitizados da planilha. O visual deve ser executivo, responsivo e inspirado na identidade visual da Porsche, com fundo claro, tipografia legível e vermelho como cor de destaque. Inclua KPIs de registros, valor total registrado, ticket médio e entregas concluídas; filtros por modelo, ano do veículo, cidade e forma de pagamento; e gráficos para valor por modelo, mix de pagamentos e registros por cidade. Faça todos os gráficos e indicadores reagirem aos filtros. Não exiba nomes de clientes, vendedores ou IDs. Como existem datas inválidas, não crie análise temporal sem dados confiáveis. Não use bibliotecas externas: mantenha HTML, CSS e JavaScript no mesmo arquivo para facilitar publicação via GitHub Pages.

Iterações aplicadas:
- Priorização de campos sanitizados e exclusão de dados pessoais desnecessários.
- Substituição de análise temporal por análises categóricas, devido às datas inválidas.
- Rótulo “valor registrado” e nota metodológica para não confundir soma bruta com receita líquida.
- Adição de filtros que atualizam simultaneamente os KPIs e os três gráficos.

## Ferramentas e uso de IA

- **ChatGPT:** apoio à análise da estrutura da planilha, definição das perguntas de negócio, elaboração do HTML/CSS/JavaScript e revisão da documentação.
- **Formato de entrega:** um único `index.html`, com estilos e lógica incorporados; não depende de bibliotecas externas.
- **Canvas:** não foi utilizado. O código foi preparado diretamente com auxílio do ChatGPT.
- **Agente com skill especializada:** não foi utilizado.

O prompt acima registra a solicitação inicial e a lista de iterações resume as principais decisões de refinamento. Se a atividade exigir capturas de tela do processo de criação, inclua evidências reais da sua execução no ChatGPT; não use capturas simuladas.

## Publicação no GitHub Pages

1. Crie um repositório **público** chamado `dio-dashboard-porsche-sales`.
2. Envie o arquivo `index.html` para a raiz do repositório.
3. Em **Settings → Pages**, selecione a publicação pela branch `main` e pela pasta `/(root)`.
4. Aguarde a publicação e teste a URL fornecida pelo GitHub Pages.
5. No envio do desafio, informe a URL do **repositório**, não apenas a URL do dashboard.

URL do dashboard: **pendente de publicação**
URL do repositório: **pendente de criação/publicação**

> Não compartilhe estes campos como se o site já estivesse no ar. Depois de publicar, substitua-os pelas URLs reais.

## Evidências recomendadas

- Captura do dashboard aberto com todos os indicadores.
- Captura de um filtro aplicado (por exemplo, selecionar um modelo e uma cidade) demonstrando que os KPIs e gráficos mudam.
- Captura das configurações do GitHub Pages ou da URL publicada funcionando.
