---
---
Kmom05 - Utvärdering av webbplatsers laddningstid och användbarhet
=========================

I den här rapporten kommer jag att undersöka tre olika webbplatser och mäta deras laddningstid och om det finns några områden de skulle kunna förbättra för att minska laddningstiden, och i så fall vilka.

Urval
-----------------------

Jag har valt att undersöka dessa tre webbplatser: SVT.se, Skatteverket, samt Wowhead. Dessa tre har valts eftersom de tillhör olika kategorier av webbplatser med olika användningssituationer och kanske lite olika målgrupp. Jag har också valt att fortsätta på samma webbsidor som i min rapport i föregående kursmoment då jag tycker att det skulle vara intressant att studera dessa tre webbsidor närmare vad det gäller fler aspekter.

Metod
-----------------------

Jag har använt Google Pagespeed och Firefox (devtools/network) för att mäta sidornas betyg enligt Google Pagespeed, antal förfrågningar, storlek på förfrågningarna, samt laddningstiden. Jag har också noterat om det enligt Google Pagespeed finns förbättringsmöjligheter för de olika sidorna som skulle kunna göra deras prestanda bättre. Slutligen har jag analyserat och jämfört de olika resultaten för att se om det finns några gemensamma problem eller särskilda skillnader mellan webbsidorna.

Resultat
-----------------------

[Klicka här för att se ett kalkylark med mätningsresultaten](https://docs.google.com/spreadsheets/d/1w_IaMsXLKCSH2xateWZ6lQcUV9vhyZUWCo8Y8V4Kq5c/edit?usp=sharing)

*Webbplats 1: SVT.se - www.svt.se*

Förbättringsområden som Google Pagespeed tog upp var följande, i ordning från störst till minst:

Mobil:

* Skjut upp inläsningen av bilder som inte visas på skärmen

* Ta bort resurser som blockerar renderingen

* Skjut upp CSS som inte används


Desktop:

* Skjut upp inläsningen av bilder som inte visas på skärmen

* Ta bort resurser som blockerar renderingen


*Webbplats 2: Skatteverket - www.skatteverket.se*

Förbättringsområden som Google Pagespeed tog upp var följande, i ordning från störst till minst:

Mobil:

* Ta bort resurser som blockerar renderingen


Desktop:

* Ta bort resurser som blockerar renderingen


*Webbplats 3: Wowhead - www.wowhead.com*

Förbättringsområden som Google Pagespeed tog upp var följande, i ordning från störst till minst:

Mobil:

* Skicka bilder i modernare bildformat

* Skjut upp inläsningen av bilder som inte visas på skärmen

* Koda bilder effektivt

* Ta bort resurser som blockerar renderingen

* Använd bilder med rätt storlek

* Minifiera JavaScript

* Skjut upp CSS som inte används

* Aktivera textkomprimering


Desktop:

* Använd bilder med rätt storlek

* Skicka bilder i modernare bildformat

* Skjut upp inläsningen av bilder som inte visas på skärmen

* Koda bilder effektivt

* Ta bort resurser som blockerar renderingen

* Skjut upp CSS som inte används

* Minifiera JavaScript


Analys
-----------------------

En klar vinnare i denna mätning är Skatteverket, med sina 100 poäng på Google Pagespeed (både mobil och desktop), och överlägsna mätvärden i Firefox. Skatteverkets hemsida har färst förfrågningar med endast 49 stycken, väger minst med sina 2,67 MB, och har en nätt laddningstid på 909 ms. Google Pagespeed hittar inte heller särskilt många förbättringsområden. Det ska kanske tilläggas att denna mätning görs på kvällen och inte i närheten av den tiden på året då självdeklarationerna ska lämnas in. Det finns inte mycket att påpeka här som skulle kunna förbättra sidan, förutom det enda området att ta bort resurser som blockerar renderingen.

Andrapristagaren är SVT.se som landar på 39 respektive 97 poäng för mobil och desktop på Google Pagespeed. Antalet förfrågningar i Firefox är 143 stycken och sidan väger in på 5,74 MB. Allt som allt tog den 1,94 s i snitt att ladda. Här finns det några få förbättringsområden enligt Google Pagespeed, med lite övervikt på den mobila sidan. Då SVT.se får bra betyg på desktop så kan de behöva jobba på sin responsivitet och de förbättringsområden som finns på den mobila sidan, som till exempel att skjuta upp inläsningen av bilder som inte visas på skärmen.

Jumboplatsen går till Wowhead som lyckats med bedriften att få betyget 1 (ett!) av Google Pagespeed på den mobila sidan, och betyget 61 för desktop. Sidan till och med känns långsam att läsa in under mätningarna. Förfrågningarna är förvisso färre än SVT.se med 115 stycken. Hela sidan väger dock in på tunga 12,29 MB och laddningstiden är 2,88 s. Google Pagespeed har mycket att säga om sidan och föreslår inte mindre än 8 förbättringar för mobil och 7 för desktop. Wowhead har mycket att göra när det gäller sin responsivitet då de får ett så lågt betyg och de kan till exempel börja med att skicka bilder i ett modernare filformat och skjuta upp inläsningen av bilder som inte visas på skärmen, då detta är de största bovarna här.

Sammanfattningsvis så kan man se att ett vanligt förbättringsområde verkar vara att ta bort resurser som blockerar renderingen, då detta område återfinns på samtliga sidor som testats i denna rapport, både på mobil och desktop. Resurser som blockerar renderingen innebär enligt Google Pagespeed att den första uppritningen av sidan blockeras av resurser som JS-kod och formatmallar, och det föreslås att man ska infoga nödvändig JS-/CSS-kod direkt på sidan och skjuta upp inläsningen av mindre kritiska kod- och formatmallar.

Ett annat vanligt förslag från Google Pagespeed är att skjuta upp inläsningen av bilder som inte visas på skärmen. Här föreslås att man låter bilder utanför skärmen och dolda bilder läsas in med s.k. lat inläsning efter att alla viktiga resurser är inlästa så att tiden till interaktivt tillstånd för sidan minskar.

En gräns för laddningstid, som jag själv skulle uppfatta som gränsen mellan en snabb och en långsam webbplats, uppskattar jag till någonstans kring 2,0 sekunder. Detta baserar jag på SVT.se:s resultat på 1,94 sekunder och att jag själv upplever sidan som helt acceptabel och inte alls seg, även om det skulle kunna gå ännu fortare. Wowhead med sina 2,88 sekunder känns däremot klart segladdad, så där har man gått över gränsen.


Referenser
-----------------------

Google Pagespeed

https://developers.google.com/speed/pagespeed/insights/


Övrigt
-----------------------

Författare: Susanna Persson

***

Detta innehåll är skrivet i markdown och man hittar innehållet i filen `content/redovisning/05_laddningstid.md`.
