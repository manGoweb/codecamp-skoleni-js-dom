# Workflow - s čím se takový JS programátor potýká

- chce rychlý a snadný vývoj
- optimalizace na produkčním prostředí
- lidé dělají chyby
- deploy
  - aktualizace dat při deployi - je zbytečné přepisovat nezměněné soubory
  - nepřepisovat uživatelská data
  - mazat cache
- různé browsery, jazyky, prostředí
- tenký / tlustý klient
- server-side / client-side
- opensource knihovny musí řešit ještě kupu dalších věcí

## rozjetí projektu - boilerplate
- version control - Git
- continuous integration - postupné nasazování nového kódu po co nejmenších celcích
- založit dokumentaci
- live reload - BrowserSync
- local server
  - web se může chovat rozdílně na http://, file:// i https://
- obrázky
  - ikony
  - responsivní velikosti

### Chrome dev tools

- elements
- network
- resources
- sources
- timeline
- profiles
- audits
- console
- record

## Environment

### vývoj

- tady píšeme zdrojový kód
- jde nám o přehlednost projektu
- snadný a rychlý vývoj

### produkce

- optimalizace
- minifikace
- concatenace
- cache
- fallbacky, polyfilly, shi(v|m)y
- bezpečnost

## Staré časy

Úprava HTML přímo na FTP. Těžko se synchronizoval stav na serveru se stavem na lokálním stroji. Ale programátoří jsou líní, tak si postupně ulehčují práci.

## Životní cyklus projektu

zahájení projektu => vývoj / spolupráce / verzování => staging => deploy => produkce


## zahájení projektu / boilerplate

- technické zázemí
- adresářová struktura
- verzovací systém
- "postahovat" nutnosti
- testovní v prohlížečích - PhantomJS, Karma
- yeoman
  - generátor projektů
  - výběr technologií
  - někdo už zpracoval best-practices
  - H5BP

### balíčkovací nástroje

Node.JS + NPM, Bower

## vývoj / development

- příprava kódu
- TDD
- vizuální TDD je těžké
- musíme testovat na různých zařízeních
- linting
- live reload
- nechceme čekat na optimalizaci obrázků a minifikaci kódu

## testování / staging

- spustit připravený kód v prostředí, které se co nejvíce blíží produkčnímu
- jednotkové testy
- integrační testy
- uživatelské testy
- snažíme se odchytit chyby dříve, než se projeví na produkci

# deploy

- Aktualizace serveru. Přesun souborů, jiná konfigurace, build assetů pro produkční použití.
- Co lze automatizovat, by mělo být automatizovno. Lidi totiž dělají chyby a zapomínají víc než stroje.

### build tools / Grunt, Gulp

- konfigurační soubor
- tasky
- spouštění
- vyvojářský režim s live-reloadem, testováním, atd.
- produkční režim vygeneruje optimalizované soubory

### precompilery a postprocesory

na produkci máme k dispozici HTML, CSS a JS. Ale vyvíjet můžeme v lepších jazycích - stačí mít "překlač" do webových jazyků.

#### preprocesory překláadjí z něčeho do webových jazyků.

- CoffeeScript => JS
- LESS, Stylus, Sass => CSS
- Jade, Mustache => HTML

#### postprocesory ladí webové jazyky

- odebírá nepotřebná pravidla - uncss
- polyfilluje standardizované vlastnosti
  - Babel pro JavaScript
  - PostCSS pro CSS

## optimalizace HTTP/1 vs HTTP/2

`HTTP/2` pragmaticky řeší optimalizační problémy, které jsme museli řešit nepříjemnými obchůzkami.

# dev stacky - boilerplate pro workflow

V mangu jsme si udělali [mango-cli](http://mangoweb.github.io/mango/).

```
npm install -g mango-cli
```

- řeší boilerplate
- řeší závislosti
- řeší serveru
- řeší produkční build
- minifikaci obrázků
- dopíšem si co zrovna potřebujem, máme to pod palcem
