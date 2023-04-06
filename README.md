# Text-based D&D hra

## Concept
Hra by měla být na bázy starých textových her jako Zork nebo Planetfall. Hráč se bude pohybovat po mapě kde může náhodně narazit na nepřátele. Mapa by měla obsahovat podzemí kde se bude odehrávat finále celé hry s finálním bossem, městečko kde si hráč bude moct koupit zbraně, lektvary, jídla a nocleh.

### Postava
Hráč si bude moct vybrat z 5 různých typů postava: 
1. **Fighter** - boj na blízko s těžkou zbrojí
2. **Mage**    - boj za pomocí kouzel a magických schopností
3. **Rogue**   - využívá momentu překvapení (stealth) a bojových triků
4. **Cleric**  - specializace na oživování a božskou magii
5. **Paladin** - bojovník který využívá výru k boji

Každá postava bude moc využít pár specifických schopností, mág na příklad bude mít schopnost vyvolat ohnivou kouli která poškodí nepřítele. Každá postava bude má své specifické hodnoty podle kterých se počítá poškození a životy. Tyto hodnoty se budou zlepšovat s každým získaným levelem.

### Rozvoj postavy
Hráč bude získávat zkušenosti za poražení nepřátel a dokončení úkolů. Po dosažení určitého množství zkušeností postava postoupí na další úroveň, čímž získá nové schopnosti a zlepší své statistiky.

### Mapa
Mapa bude tvořena několika oblastmi:
- Městečko: Místo, kde hráč může nakupovat zbraně, lektvary a jídlo, najít si nocleh a získat úkoly od místních obyvatel.
- Lesy: Oblasti s náhodnými setkáními s nepřáteli a skrytými poklady.
- Podzemí: Zde se nachází finální boss a největší výzvy. Hráč musí být dobře připraven, než se sem vydá.

### Bojový systém
Boje budou probíhat v textové formě s výběrem akcí. Hráč bude moct zvolit, zda chce zaútočit, použít schopnost, použít předmět nebo utéct. Boj bude probíhat na základě střídání tahů, kde hráč i nepřítel budou mít možžnost provést jeden tah za kolo.

### Inventář a předměty
Hráč bude mít k dispozici inventář, kde může uchovávat zbraně, zbroj, lektvary, jídlo a další předměty. Některé předměty budou mít jednorázový efekt (např. lektvary), zatímco jiné budou sloužit k vylepšení postavy (zbraně, zbroj). Předměty budou mít různé hodnoty a vlastnosti, které ovlivňují účinnost v boji.

### Příběh a úkoly
Hra bude mít hlavní příběhovou linii, která se bude rozvíjet postupem hráče. Hráč bude také mít možnost plnit vedlejší úkoly, které mu poskytnou zkušenosti, peníze nebo předměty. Vedlejší úkoly budou zahrnovat například záchranu unesených vesničanů, hledání ztracených artefaktů nebo vyčištění oblasti od nepřátel.

### Interakce s NPC
Hráč bude mít možnost komunikovat s různými NPC (nehráčskými postavami) ve městě a v jiných oblastech. Tyto interakce mohou zahrnovat obchodování, získávání informací a úkolů nebo vyjednávání.

### Náhodná generace
Náhodná generace
Aby byla hra pokaždé jiná a zajímavá, bude náhodně generovat některé aspekty hry, jako jsou umístění nepřátel, poklady nebo úkoly. Tím se zvýší opakovatelnost hry a hráči budou mít možnost zažít nové situace a výzvy.

## Tvorba postavy a generování statistik
Při tvorbě postavy hráč nejprve zvolí jeden ze 5 povolání (Fighter, Mage, Rogue, Cleric, Paladin). Poté bude mít možnost rozdělit si body mezi základní statistiky postavy. Tyto statistiky budou:
1. **Síla (STR)**        - ovlivňuje fyzické poškození a schopnost nést těžší zbroj.
2. **Obratnost (DEX)**   - ovlivňuje šanci na úspěšný útok, unik a schopnost používat lehké zbraně.
3. **Inteligence (INT)** - ovlivňuje magické schopnosti, počet kouzel, které může postava naučit a jejich účinnost.
4. **Vitalita (CON)**    - ovlivňuje maximální množství životů postavy a rychlost regenerace.
5. **Charisma (CHA)**    - ovlivňuje interakce s NPC a vyjednávání.

Každá postava začíná s určitým počtem bodů, které může rozdělit mezi základní statistiky. Tyto body mohou být přiděleny následovně:

- **Fighter**: STR 12, DEX 8, INT 6, CON 10, CHA 6
- **Mage**: STR 6, DEX 6, INT 12, CON 8, CHA 10
- **Rogue**: STR 8, DEX 12, INT 6, CON 8, CHA 8
- **Cleric**: STR 8, DEX 6, INT 10, CON 10, CHA 8
- **Paladin**: STR 10, DEX 8, INT 8, CON 10, CHA 6

Hráč pak dostane dalších 10 bodů, které může rozdělit mezi statistiky dle svého uvážení. Během hry postava získává další body, které může přidělovat při postupu na další úroveň.

## Generování zbraní
Při generování zbraní jako lootu pro hráče je důležité zohlednit několik aspektů, jako je úroveň hráče, typ zbraně a bonusy. Následující algoritmus může být použit pro výpočet statistik zbraní při jejich tvorbě:
1. **Určit úroveň zbraně**: Zbraň by měla mít úroveň, která je podobná úrovni hráče, aby byla pro hráče užitečná. Tuto úroveň lze určit následovně:
- Pokud je hráč na úrovni 1-5, generovat zbraň Tier 1.
- Pokud je hráč na úrovni 6-10, generovat zbraň Tier 2.
- Pokud je hráč na úrovni 11-15, generovat zbraň Tier 3.
- A tak dále.

1. **Typ zbraně**: Na základě povolání postavy bude generována zbraň, která je pro dané povolání vhodná. Například, pro bojovníka bude generována zbraň na blízko, zatímco pro mága bude generována hůl.
2. **Výpočet základních statistik**: Základní statistiky zbraně, jako je útok, kritický zásah nebo přesnost, by měly být vypočítány na základě úrovně zbraně. Například, zbraň Tier 1 by mohla mít základní útok v rozmezí 1-5, zatímco zbraň Tier 2 by mohla mít základní útok v rozmezí 6-10.
3. **Bonusy a vlastnosti**: Na základě náhodného generování mohou zbraně obsahovat různé bonusy a vlastnosti, které ovlivňují jejich účinnost v boji. Tyto bonusy mohou zahrnovat například zvýšení šance na úspěšný útok, šance na kritický zásah nebo odolnost proti určitým typům poškození.

Příklad generování zbraně pro postavu na úrovni 5 s povoláním bojovník:
- Hra vybere meč jako vhodný typ zbraně pro bojovníka.
- Jelikož postava je na úrovni 5, hra vybere zbraň Tier 2.
- Hra náhodně vybere bonusy a vlastnosti zbraně, například +5% k rychlosti útoku a +10% k odolnosti proti ohnivému poškození.

Příklad výpočtu statistik zbraně pro hráče na úrovni 7:
1. Určit úroveň zbraně: Hráč je na úrovni 7, takže zbraň bude Tier 2.
2. Určit typ zbraně: Hráč je bojovník, takže bude generován meč.
3. Výpočet základních statistik: Pro zbraň Tier 2 bude základní útok v rozmezí 6-10. Generujeme náhodné číslo v tomto rozmezí, například 8. Stejně tak pro další statistiky, jako je kritický zásah nebo přesnost. Například:
 - Kritický zásah: 10% (náhodně vygenerováno)
 - Přesnost: 85% (náhodně vygenerováno)
4. Náhodné bonusy: Pro zbraň Tier 2 mohou být náhodné bonusy v rozmezí 1-3. Generujeme náhodné číslo v tomto rozmezí pro různé bonusy, například:
- Šance na kritický zásah: +2% (náhodně vygenerováno)
- Šance na úspěšný útok: +5% (náhodně vygenerováno)

Výsledná zbraň pro hráče na úrovni 7 by tedy měla následující statistiky:
- Úroveň zbraně: Tier 2
- Typ zbraně: Meč
- Základní útok: 8
- Kritický zásah: 10% + 2% (bonus) = 12%
- Přesnost: 85%
- Úspěšnost: 75% + 5% (bonus) = 80%

Vytvořené zbraně by měly být adekvátní pro úroveň hráče a umožnit hráči pokrok v hře.

## Logika náhodných soubojů
Náhodné boje by měly být založeny na pravděpodobnosti, která závisí na oblasti, ve které se hráč nachází. Tato pravděpodobnost by měla být vyšší v nebezpečných oblastech, jako jsou jeskyně nebo lesy, a nižší v oblastech, kde jsou méně nepřátel, jako jsou vesnice nebo silnice. Následující algoritmus generuje náhodné boje v různých oblastech:

1. Určit pravděpodobnost boje pro každou oblast.
2. Pro každý tah hráče v dané oblasti generovat náhodné číslo (1-100).
3. Pokud je náhodné číslo menší než pravděpodobnost boje, dojde k náhodnému boji.

Příklad pravděpodobnosti boje:

- Jeskyně:       60%
- Les:           40%
- Vesnice:       5%
- Silnice/Cesta: 10%

### Výpočet poškození
Poškození v boji závisí na statistikách postavy, zbraně a nepřítele. Výpočet poškození by měl brát v úvahu následující aspekty:

1. **Útok**: Základní útok je určen statistikou postavy a zbraně. Například, pro bojovníka je útok založen na síle (STR), zatímco pro mága je útok založen na inteligenci (INT).
2. **Kritický zásah**: Je určen statistikou postavy a zbraně. Pokud dojde k kritickému zásahu, poškození se zvýší o určitý násobek.
3. **Přesnost**: Určuje šanci na úspěšný útok. Přesnost je založena na obratnosti (DEX) postavy a zbraně.
4. **Odolnost**: Určuje, jaké množství poškození je blokováno. Odolnost je založena na statistikách postavy a zbraně.
5. **Typ poškození**: Typ poškození může být magický, fyzický nebo ohnivý. Různí nepřátelé mají různé slabiny a odolnosti proti různým typům poškození.

Algoritmus pro výpočet poškození:

1. Určit základní útok na základě statistik postavy a zbraně.
2. Určit kritický zásah na základě statistik postavy a zbraně. Pokud dojde k kritickému zásahu, zvýšit poškození o určitý násobek.
3. Určit přesnost útoku na základě statistik postavy a zbraně. Pokud útok minul, poškození bude nulové.
4. Určit odolnost proti poškození na základě statistik nepřítele.
5. Aplikovat typ poškození a zohlednit slabiny a odolnosti nepřítele proti různým typům poškození.
6. Vypočítat konečné poškození jako základní útok plus kritický zásah, mínus odolnost, a upravit podle typu poškození.

Příklad výpočtu poškození:

1. Bojovník s mečem má základní útok 15 (10 ze síly a 5 ze zbraně).
2. Bojovník má 10% šanci na kritický zásah, který zvyšuje poškození o 50%. Při kritickém zásahu je poškození 22,5 (15 * 1,5).
3. Bojovník má přesnost 75% (založeno na obratnosti a zbraní). Pokud útok minul, poškození bude 0.
4. Nepřítel má odolnost 5 proti fyzickému poškození.
5. Bojovník způsobuje fyzické poškození a nepřítel nemá žádnou speciální slabost ani odolnost proti tomuto typu poškození.
6. Konečné poškození je 10 (15 - 5) pro normální útok nebo 17,5 (22,5 - 5) pro kritický zásah.

Tímto způsobem se vypočítává poškození v boji. Tento algoritmus lze použít i pro výpočet poškození způsobeného nepřítelem hráči. V takovém případě budou statistiky postavy nahrazeny statistikami nepřítele a naopak.

### Interakce zbraně a postavy
Pro interakci statistik zbraní se statistikami postav můžete použít následující logiku:
1. **Základní útok**: Přidejte hodnotu základního útoku zbraně ke značce síly (STR) postavy, abyste získali celkový základní útok.
2. **Kritický zásah**: Použijte kritický zásah zbraně jako základní hodnotu. Poté přidejte bonusy na základě obratnosti (DEX) postavy. Například můžete přidat 1% za každých 5 bodů obratnosti.
3. **Přesnost**: Přidejte hodnotu přesnosti zbraně k hodnotě obratnosti (DEX) postavy a poté ji podělte dvěma, abyste získali celkovou přesnost útoku.
4. **Úspěšnost**: Spočítejte celkovou úspěšnost kombinací statistiky úspěšnosti zbraně a statistiky inteligence (INT) postavy. Například můžete přidat 1% za každých 5 bodů inteligence.

Nyní aplikujeme tuto logiku na příklad bojovníka s následujícími statistikami a zbraní:

**Postava (Fighter)**:
STR 12, DEX 8, INT 6, VIT 10, CHA 6

**Zbraň**:
Úroveň zbraně: Tier 2
Typ zbraně: Meč
Základní útok: 8
Kritický zásah: 12% (10% + 2% bonus)
Přesnost: 85%
Úspěšnost: 80% (75% + 5% bonus)

**Výsledné statistiky**:

1. Základní útok: 12 (STR) + 8 (zbraň) = 20
2. Kritický zásah: 12% (zbraň) + (8 DEX / 5) * 1% = 12% + 1.6% = 13.6%
3. Přesnost: (85% (zbraň) + 8 (DEX)) / 2 = (85 + 8) / 2 = 46.5%
4. Úspěšnost: 80% (zbraň) + (6 INT / 5) * 1% = 80% + 1.2% = 81.2%

### Kouzla a bojové schopnosti
Příklad kouzel a schopností pro každou z postav:

**Fighter**:
1. Útok silou: Přidejte bonus k poškození na základě hodnoty síly (STR).
2. Odpoutání: Na krátkou dobu zvýší obranu a sníží příchozí poškození.
3. Rozzuření: Zvyšte rychlost útoku a poškození za cenu snížení obrany.

**Mage**:
1. Ohnivá koule: Způsobí poškození ohně cílům v určité oblasti.
2. Bleskový šok: Útočí na jednoho cíle s elektrickým poškozením a má šanci paralyzovat.
3. Ledová bariéra: Vytvoří ochrannou bšarieru kolem postavy, která sníží přijímané poškození.

**Rogue**:
1. Zákeřný útok: Útočí na cíl zpoza a způsobuje zvýšené poškození.
2. Kapesní loupež: Pokus o ukradení předmětů z cíle.
3. Rychlé unikání: Zvyšuje šanci na unik před nepřáteli.

**Cleric**:
1. Léčivé světlo: Léčí cíl na základě hodnoty Inteligence (INT).
2. Vzkřísit: Oživí padlého spoluhráče s částí jeho životů.
3. Posvěcený štít: Poskytuje ochranu proti zlým bytostem a magii.

**Paladin**:
1. Světelný úder: Útočí na cíl a způsobuje světelné poškození.
2. Božská intervence: Poskytuje krátkodobou nesmrtelnost a obranu proti všem útokům.
3. Posvěcená zbraň: Zvýší poškození zbraně s božským požehnáním na omezenou dobu.

## Shrnutí
Hra bude založena na klasických textových adventurách, ale s prvky RPG a fantasy světa. Hráči budou moci prozkoumávat různé oblasti, bojovat s nepřáteli, rozvíjet své postavy a odhalovat příběh. Díky náhodné generaci a množství možností bude hra zajímavá a poutavá pro mnoho hráčů.
