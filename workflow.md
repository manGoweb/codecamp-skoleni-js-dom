# Workflow

zahájení projektu => vývoj => spolupráce / verzování => staging => deploy => produkce

topics:
- rychlý a snadný vývoj
- optimalizace na produkčním prostředí
- lidské chyby !
- aktualizace dat - je zbytečné přepisovat nezměněné soubory
- uživatelská data nepřepsat
- cache smazat
- různé browsery, jazyky, prostředí
- tenký / tlustý klient
- server-side / client-side
- problémy opensource aplikace pro různá prostředí

## rozjetí projektu - boilerplate

yeoman

testovní v prohlížečích - karma

version control

continuous integration

dokumentace

live reload

local server

image generating - icons, responsive sizes

unused css, repeating rules

linting

všechny platformy už dlouho buildují - web není o moc jiný


Chrome dev tools

- elements
- network
- resources
- sources
- timeline
- profiles
- audits
- console
- record

H5BP

coding style, coding methodologies

BEM

modernizr



## Nevyvíjet znova kolo

Hodně věcí už někdo napsal před vámi, možná i lépe.

### balíčkovací nástroje

Node.JS + NPM, Bower

## Environment

- vývoj
  - tady píšeme zdrojový kód
  - jde nám o přehlednost projektu
  - snadný a rychlý vývoj
- produkce
  - optimalizace
  - minifikace
  - concatenace
  - cache
  - fallbacky, polyfilly, shi(v|m)y
  - bezpečnost

## Staré časy

Úprava HTML přímo na FTP. Těžko se synchronizoval stav na serveru se stavem na lokálním stroji.

# Deploy

Aktualizace serveru. Přesun souborů, jiná konfigurace, build assetů pro produkční použití.

Maintenance režim

Co lze automatizovat, by mělo být automatizovno.
Lidi dělají chyby a zapomínají. Víc než stroje.

## zahájení projektu / boilerplate

- technické zázemí
- adresářová struktura
- verzovací systém
- "postahovat" nutnosti

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
- snažíme se odchytit chyby dříve, než se projeví na produkci

## Build tools / Grunt, Gulp

- konfigurační soubor
- tasky
- spouštění

## precompilery a postprocesory

na produkci máme k dispozici HTML, CSS a JS. Ale vyvíjet můžeme v lepších jazycích - stačí mít "překlač" do webových jazyků.

preprocesory překláadjí z něčeho do webových jazyků.
- CoffeeScript => JS
- LESS, Stylus, Sass => CSS
- Jade, Mustache => HTML

postprocesory ladí už samotné webové jazyky.
- odebírá nepotřebná pravidla
- polyfilluje standardizované vlastnosti

# optimalizace HTTP/1 vs HTTP/2

HTTP/2 pragmaticky řeší optimalizační problémy, které jsme museli řešit nepříjemnými obchůzkami.

# dev stacky - boilerplate pro workflow

V mangu jsme si udělali mango-cli.

npm install -g mango-cli

- řeší boilerplate
- řeší závislosti
- řeší serveru
- řeší produkční build
- minifikaci obrázků
- dopíšem si co zrovna potřebujem, máme to pod palcem
