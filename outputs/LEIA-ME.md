# Olivas — Caderno de Coquetelaria

Aplicativo responsivo em HTML, CSS e JavaScript puro. Não usa backend. O menu e os favoritos ficam no `localStorage` do navegador/dispositivo.

## Abrir no computador

Para uma visualização rápida, abra `index.html` no navegador. A experiência PWA, instalação e cache offline precisam de um servidor local ou de publicação HTTPS.

Com Python instalado, abra um terminal nesta pasta e execute:

```bash
python -m http.server 8000
```

Depois acesse `http://localhost:8000`.

## Publicar e instalar

Publique o conteúdo desta pasta em qualquer hospedagem estática com HTTPS, preservando os nomes e caminhos dos arquivos. O manifesto, o ícone SVG e o service worker habilitam instalação e funcionamento offline depois do primeiro acesso. A fonte decorativa pode depender de conexão; as fontes de sistema continuam disponíveis offline.

## Dados e manutenção

- **Destilados** apresenta país/região de origem, história da família, matéria-prima, características de aroma e estilo, cinco rótulos de referência e três exemplos de coquetéis para cada tipo: vodka, gin, rum, whisky/whiskey, Cognac, cachaça e tequila. Algumas origens são disputadas ou regionais; o texto sinaliza esses casos. Rótulos e coquetéis são exemplos didáticos.
- **IBA** reúne 102 coquetéis nas três categorias oficiais, com ingredientes e quantidades, modo de preparo e guarnição traduzidos das fichas. Quando há uma história com fonte histórica confiável, ela aparece com link de referência; drinks sem história confirmada não exibem essa seção. O link da receita abre a ficha oficial da IBA. Catálogo consultado em 30/09/2026.
- **Prova** reúne 300 perguntas sobre coquetéis, técnicas, insumos, destilados e história, com 100 por dificuldade. Cada prova sorteia 20 questões sem repetir a prova imediatamente anterior na mesma dificuldade. Ao escolher uma alternativa, a interface informa na hora se está certa; quando há erro, destaca a resposta correta e mostra uma explicação. Ao final, apresenta nota, gabarito e comentários.
- **Olivas** começa com 32 receitas transcritas do PDF `drinks.pdf` enviado. Os nomes e valores vêm do arquivo, mas a extração de texto tinha acentos corrompidos e algumas associações de guarnição/medida podem exigir conferência com a equipe. Todos aparecem como transcrição, não como validação oficial.
- Use **Menu** para cadastrar, editar ou remover itens. **Restaurar transcrição do PDF** retorna a lista inicial deste aplicativo.
- Dentro de **Olivas**, navegue pelos grupos **Autorais**, **Releituras**, **Sem álcool**, **Clássicos** e **Gin e caipiras**. Ao cadastrar ou editar um drink, escolha o grupo em que ele deve aparecer.
- **Exportar backup** salva os dados locais em JSON. **Importar backup** substitui os dados locais pelo conteúdo do arquivo escolhido.
- Os dados ficam somente no dispositivo e no perfil do navegador usados. Exporte um backup antes de trocar de aparelho ou navegador.

## Arquivos

- `index.html` — estrutura e interface.
- `style.css` — visual responsivo.
- `app.js` — menu, busca, filtros e armazenamento local.
- `iba-data.js` — fichas locais de coquetéis IBA, com links para as páginas de origem.
- `iba-history.js` — histórias com fonte externa identificada; drinks sem história confirmada não exibem a seção.
- `study-data.js` — banco local com 300 questões para provas offline.
- `manifest.webmanifest`, `icon.svg`, `sw.js` — instalação e suporte offline.
- `assets/` — fotografias enviadas, aplicadas como fundos com sobreposição escura para preservar o contraste do texto.

## Referências

- [Regulamento europeu 2019/787](https://eur-lex.europa.eu/eli/reg/2019/787) — categorias e definições de destilados.
- [ScienceDirect — resumo sobre vodka](https://www.sciencedirect.com/topics/food-science/vodka).
- [Historic England — história do gin na Inglaterra](https://historicengland.org.uk/images-books/publications/gin-and-the-english/).
- [BNIC — história oficial da denominação Cognac](https://www.cognac.fr/en/discover/a-unique-spirit/one-culture-une-histoire/).
- [Brasil — Decreto 4.062/2001 sobre a indicação geográfica Cachaça](https://www.planalto.gov.br/ccivil_03/decreto/2001/d4062.htm).
- [Consejo Regulador del Tequila — origem e história](https://www.crt.org.mx/nuestro-tequila/).
- [Historic England — história do gin na Inglaterra](https://historicengland.org.uk/images-books/publications/gin-and-the-english/).
- [Visit Barbados — história do rum em Barbados](https://www.visitbarbados.org/discover/island-stories/rum).
- [Scotch Whisky Association — história do Scotch](https://www.scotch-whisky.org.uk/discover-scotch/story-of-scotch/).
- [Embrapa — história e produção da cachaça](https://www.embrapa.br/en/web/agencia-de-informacao-tecnologica/cultivos/cana-de-acucar/pos-producao/cachaca).
- [International Bartenders Association — All Cocktails](https://iba-world.com/cocktails/all-cocktails/) — catálogo e categorias IBA.
- [Difford’s Guide — histórias de coquetéis](https://www.diffordsguide.com/cocktails/tales-behind-the-cocktails) — referências históricas para os drinks que têm seção de história no aplicativo.
