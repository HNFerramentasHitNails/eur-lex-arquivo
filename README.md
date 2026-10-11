# Arquivo de direito da UE em português — complemento de `eur-lex`

Complemento do repositório [HNFerramentasHitNails/eur-lex](https://github.com/HNFerramentasHitNails/eur-lex)
(legislação da UE em vigor, leis portuguesas de transposição, orientações). Aqui ficam as colecções grandes,
em Markdown, obtidas do Cellar (Serviço das Publicações da UE) em 2026-10-11 com
`ferramentas/arquivo.py` do repositório principal:

| Pasta | O que tem | Quantidade |
|---|---|---|
| `jurisprudencia/<ano>/<CELEX>.md` | Acórdãos, despachos, conclusões de advogados-gerais e pareceres do Tribunal de Justiça, do Tribunal Geral e do Tribunal da Função Pública com texto em português. `INDICE.tsv` tem a coluna `interpreta` (actos interpretados). | 38 995 com texto; 2 062 da lista sem texto em português |
| `ue-revogada/<tipo>/<ano>/<CELEX>.md` | Legislação que o Cellar marca como não estando em vigor: última versão consolidada com texto em português ou, se não houver, o original do Jornal Oficial. Serve para saber que regra se aplicava antes. | 48 579 com texto; 3 916 sem texto em português |
| `propostas/<ano>/<CELEX>.md` | Propostas legislativas da Comissão (COM). Podem ter sido adoptadas com alterações, retiradas ou estar em negociação; o estado do processo está no EUR-Lex. | 16 288 com texto; 2 696 sem texto em português |

Cada pasta tem um `INDICE.tsv` (celex, data, tipo, título, tipo de texto, tamanho, ficheiro). Cada ficheiro começa
com metadados YAML (`celex`, `titulo`, `data_documento`, `url_eurlex`, `obtido_em`, …).

**Atenção:** nada disto é direito em vigor. A legislação em vigor está no repositório principal (`ue/`).
Os textos consolidados não têm valor jurídico; fazem fé os textos publicados no Jornal Oficial.

Não é actualizado automaticamente: para refazer, no repositório principal,
`python3 ferramentas/arquivo.py tudo <jurisprudencia|revogada|propostas> --raiz ../eur-lex-arquivo`.

**Fonte e licença:** EUR-Lex, © União Europeia, 1998-2026, obtido através do Cellar. Reutilização autorizada
para fins comerciais ou não comerciais (Decisão 2011/833/UE). Alterações: conversão de HTML para Markdown e
acrescento de metadados.
