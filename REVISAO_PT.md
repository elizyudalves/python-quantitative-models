# Revisão inicial do portfólio

## Escopo
ZIP original: 219 entradas, incluindo diretórios, checkpoints, dados e resultados. Foram encontrados 28 notebooks fora dos checkpoints. Não são 28 modelos independentes. Foi feita triagem estática dos notebooks e leitura mais detalhada dos dois selecionados e dos casos abaixo; não uma auditoria integral de todas as estratégias.

## Achados confirmados
- `Regressaolinearelogistica.ipynb`: `model.fit(X, y)` e `predict_proba(X)` usam a mesma amostra. A curva não demonstra generalização. Separar cronologicamente treino/validação/teste e ajustar transformações somente no treino.
- `PERCENTIL.ipynb`: treino/teste é dividido após o cálculo do backtest e não governa a avaliação. `risk / price` representa alocação nocional, não risco limitado por stop. A curva contabiliza resultados realizados, omitindo perdas/ganhos abertos. Entradas usam o fechamento que gera o sinal.
- `garchcustoagressao.ipynb`: AggBuy/AggSell usam números aleatórios sobre o volume, explicitamente como placeholder. Isso não é fluxo observado.
- `Testegarchcommédias.ipynb` e `reversãomediaregimeGARCH.ipynb`: código extraído idêntico.
- Há notebooks vazios e fragmentos sem contexto, inadequados como projetos independentes.
- `backtest5variaveis.ipynb`: possui validação de OHLCV, variáveis diárias defasadas, execução na abertura seguinte e relatórios. Contudo, custos e slippage padrão são zero, quantidade é nocional fracionária e não há stop/alvo fixo nem validação fora da amostra. As sessões excluídas devem ser reportadas.
- `Garchsemanal.ipynb`: usa GARCH(1,1) com distribuição t e agrega variâncias de 1/5/21 pregões. O ranking é de volatilidade, apesar da referência a liquidez no cabeçalho original. Não mede vantagem de negociação. Falta avaliação de previsões fora da amostra e diagnóstico de convergência/resíduos.

## Preparação realizada
Dois notebooks selecionados, nomes padronizados, documentação em inglês e instruções de execução. Saídas e metadados locais removidos. Código analítico preservado, sem alterações nas regras. Não incluídos dados brutos, planilhas e relatórios antigos: proveniência, permissões e correspondência com versões de código ainda não foram verificadas. Os originais continuam no ZIP enviado.

## Verificações
JSON dos notebooks e sintaxe das células Python selecionadas verificados. Busca estática por credenciais: nenhuma credencial preenchida identificada nos dois notebooks selecionados; usam configuração vazia ou variáveis de ambiente. Isso não equivale a garantia sobre todos os arquivos do ZIP original. Não executados downloads, ajustes GARCH ou backtests. Dependências inferidas, não fixadas/testadas em ambiente completo.

## Publicação
1. Extraia o ZIP preparado.
2. No repositório criado, envie README.md, requirements.txt, INVENTARIO.md, REVISAO_PT.md e a pasta projects. Não envie o ZIP como substituto dos arquivos navegáveis.
3. Preserve ou atualize o .gitignore existente; inclua as exclusões do arquivo preparado.
4. Antes de publicar, complete os créditos e confirme autorização para trechos derivados de terceiros.
5. Mensagem de commit sugerida: Add documented GARCH and VWAP research notebooks.
6. Depois confira a renderização dos dois notebooks e os links do README.

## Próxima prioridade
Execute os dois notebooks em ambiente limpo e registre versões, período de dados, falhas e exclusões. Em seguida, implemente uma avaliação cronológica com amostra não usada para escolher parâmetros. Para candidaturas, explique uma hipótese, uma decisão técnica e uma limitação de cada estudo. Não publique nove projetos incompletos apenas para aumentar a contagem.
