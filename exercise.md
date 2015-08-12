# Cvičení - středa

Vytvořte jednoduchého správce úkolů. Každý úkol má svůj název a termín dokončení. Jako úložiště použijte [LocalStorage](http://devdocs.io/dom/web_storage_api/using_the_web_storage_api). Dnes neřešte vzhled.

## Wireframe

```
Úkolovníček

-----------------------------------------
| Přidej tudůčko...            | termín |      Přidej
-----------------------------------------

 | |  Vynést koš                | zítra |
-----------------------------------------
 |x|  Napsat cvičení            |  ASAP |
-----------------------------------------
 | |  Zavolat mamince       | next week |
-----------------------------------------

Zbývají 2 úkoly | Filtrování: *All* | Active | Completed
```

// Inspirováno: http://todomvc.com/examples/vanillajs


## Cvičení - čtvrtek

I. Dejte úkolovníčku pohledný kabátek (na rozehřátí ;)
I. Rozšiřte správce úkolů o podporu offline režimu (včetně načtení stránky v offline)
II. a následnou synchronizaci se serverem při dostupnosti připojení.
III. Dále umožněte současné vkládání a editaci položek více uživateli na jednou, se zachováním pořadí vložení (tip: čas vytvoření).
IV. BONUS: Umožněte vkládání a přehrávání zvukových poznámek.

Pokyny:
- použijte [Application cache](https://developer.mozilla.org/en-US/docs/Web/HTML/Using_the_application_cache)
- můžete využít [WebSockets](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API) ale nemusíte, stačí obyčejný polling (pravidelné dotazování serveru)
- zanedbejte uživatelské účty i autorizaci
- backend použijte dle libosti, klidně jeden server do týmu
- zajistěte správné vyřešení konfliktních situací (dva uživatelé upravují todo najednou)

