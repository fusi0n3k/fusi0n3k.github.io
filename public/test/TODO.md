# LaTeX GenIUS TODO

## Lingue

- [ ] Questione \PassOptionsToPackage: è necessario precaricare i linguaggi o no?
- [ ] Togliere lingue rare da `genius.sty` e aggiungere `\PassOptionsToPackage{lang}{babel}` agli articoli
- [ ] Caricare pacchetti specifici per lingue (es. `lh`) solo se lingua è caricata

## Spaziatura

- [x] In Magazine lo spazio prima di sommario e abstract è maggiore di quello che c'è in online-first

## Sommario generale

- [ ] Far funzionare hyperref a parti (Focus, Interventi...)
- [x] Diminuire spazio tra Titolo Parte e Autore/articolo

## Footnotes

- [ ] `itemize,enumerate` togliere spazio fra items (v. 24-01/05-caroli note 11, 47)
- [x] La linea di separazione delle note va spostata a sx
- [x] Impedire che le note vadano sotto il margine

## Sommario articoli

- [ ] Alcuni a-capo continuano a non funzionare (24-1/02-goisis; 24-1/10-moro)

## Sezioni, sottosezioni, sottosottosezioni, paragrafi

- [ ] Fare in modo che primo paragrafo dopo `\paragraph{}` non sia indentato (v. 24-02/03-davies); adesso viene messo un `\noindent` da vertoplugin

## Liste

- [ ] Uniformare linee/lettere/numeri, indentazioni e secondi paragrafi (v. 03-davies; 08-sulpizi; 09-capuozzo, 24-01/10-moro)

## PDF

- [ ] Indice: aggiungere capitoli (Focus, Interventi, etc)

## Inizio articolo

- [ ] Prevedere articolo senza abstract, sommario, sezione non numerata, nessuna sezione (24-01/01-pelissero)

## PHP

- dom: url fare maggiore attenzione che alcuni vengono spezzati (24-2/03-davies linea 1167 dopo importazione ma prima di texdom - anche linea 100, 222)
- certi `\textquotesingle` non vengono trasformati (24-2/03-davies l 634)
- enumerate/itemize (v. 24-2/08-sulpizi) togliere quanto aggiunto (viene messo da genius.sty)

## Note di redazione

- Fare presente che l'Abstract va SEMPRE in Italiano e Inglese, anche se l'articolo è in spagnolo, russo, etc...
- Il Sommario degli articoli VA limitato alle sottosezioni (alcune volte ci sono anche le sottosottosezioni)
- Strutture come quelle di 12-massaro andrebbero evitate; non 
  - 6\. Un possibile percorso di riforma: a) dalla gender-based violence ai gender-based crimes
  - 6.1. b) introduzione di una circostanza aggravante comune

  ma:

  * 6\. Un possibile percorso di riforma
  * 6.1. Dalla gender-based violence ai gender-based crimes
  * 6.2. Introduzione di una circostanza aggravante comune

## Ricorda che:

### A capo:

- Se due parole unite da una barra (Parola/Parola) non vengono sillabate, usa `Parola\slash Parola`
- Se un `\url{xxx}` non viene sillabato, usare `\href{xxx}{xxx}`
- Se in un titolo sezione si vuole inserire uno o più aCapo forzati, usare `\section[Titolo senza aCapo]{Titolo\\conAcapo}`
- Sommario Generale: per forzare cambio pagina, usare `\addtocontents{toc}{\vspace{3cm}}`: (Esempio:`\include{08-sulpizi ¶ \addtocontents{toc}{\vspace{3cm}}% ¶ \Interventi`)
- Forzare newline mantenendo giustificazione: \linebreak

### Altro:

- Per inserire nota all'interno di:
  - titolo sezione: `\section[Titolo sezione]{Titolo\footnote{Testo Nota} sezione}`
  - titolo articolo: `\articleTitle[Titolo articolo]{Titolo\footnote{Testo Nota} sezione}`
- Per info autore in lingua diversa dalla principale: `\articleAuthorsInfo[lingua]{Info}`
- Se in articolo manca sommario locale, aggiungere `\spacerNoArticleToc` prima di `\makeabstract{}`
- Se un articolo inizia senza sezione (direttamente con testo), aggiungere `\spacerNoSectionAtStart` dopo `\makeabstract{}`

## Routines:
- `-` `--` `---`
- `\textbar` (Evidenziata, proporre di cambiare con : o -)
- `url` `href`
- `\textgreater{}`