# Od AI slopu k rozumné kreativě - blok Radim Kracík (13. 10. 2026, 10:35 až 11:15)

Šablona postavená 1:1 na deckech Jakuba (Blok 1) a Lukáše (Blok 0, 2, 3).
Hlavička (CSS, fonty, tokeny, navigace, presenter) je identická s jejich decky, neměnit.

## Soubory

- `index.html` - deck, otevřít v Chrome/Edge přímo ze souboru
- `presenter.html` - presenter view (aktuální + další slide, poznámky, stopky 40 min); v decku klávesa `P`
- `assets/` - fonty, loga, ribbon; `assets/ukazky/` zmenšené kreativy Mexický týden (dif-* difuzní modely, mcp-* GIMP přes MCP, safe-* přeskládané do bezpečného čtverce), originály v `C:\Users\kraac\Downloads\ukazky-prezentace`
- `assets/video/` - ukázky videí ke slidu R-12c (loison-reels.mp4 = Tomáš hook A (mužský hlas, loison_reels_tomas_hookA.mp4) z C:\workspace\loison-reels, svoboda-vykup.mp4 = vykup_bytu_praha_draft01 z C:\workspace\svoboda-meta-export\video-vykup), překódováno na 720x1280 + poster jpg; mezerník nad videem ovládá video, ne slide
- Slidy R-12e až R-12j (video generátory, tísnivé údolí): oba grafy jsou inline SVG překreslené podle Moriho (Wikimedia), foto zombie = záběr z filmu Úsvit mrtvých 2004 (usvit-mrtvych.jpg, cizí materiál, jen pro přednášku). Slop ukázky R-03b: slop-*.jpg (Trump/Variety, Trikolora/Novinky.cz, Rohlík, slovenský plakát Balog) jen pro interní workshop.
- `_preskladani/` - podklady ke slidu R-10: `brief*.md` (společné zadání + per model), `in/` zdrojové XCF a PNG, `out/` výsledky (png master 1080x1920, xcf s vrstvami, *-ctverec.png = ořez 1:1), `out-v1-png/` první pokus Fable z PNG bez vrstev. Astra a Sol 6 běžely přes Codex (gpt-6-astra, gpt-6-sol), Opus 5.5 a Fable 5.1 jako Claude subagenti, všichni sériově v jednom GIMPu.

## Jak doplňovat slidy

- Každý slide = `<section class="slide">` a nad ním HTML komentář `<!-- R-XX · popisek -->`. Presenter z komentáře bere název slidu.
- Poznámky pro lektora do atributu `data-notes="..."` na `<section>`.
- Střídat `.slide` a `.slide.soft` (světlejší závoj) kvůli rytmu pozadí.
- `.r` = prvek se odhalí při příchodu na slide, `.r-children` = děti postupně.
- Vlastní třída `.gallery` (4 stojaté kreativy vedle sebe, `.gallery.one` = jedna velká), `figure.todo .ph` = zástupný rámeček.
- `[TODO]` = místo k doplnění. Nepotřebné vzorové slidy smazat, počet slidů se přepočítá sám (číslo v `id="tot"` je jen výchozí hodnota).
- Kicker drží tvar `AI kreativa · podtéma`, ať to ladí s `Blok 1 · ...` a `Blok 2 · ...` u kolegů.
- Zdroj dole na slidu: `<div class="source">...</div>`, u faktů s datem "Stav k 13. 10. 2026".

## Zdrojové decky

Rozbalené v `C:\workspace\effectix-ai-workshop\_in\` (lukas, jakub) pro inspiraci a kopírování layoutů.
