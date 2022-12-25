---
Title: Design Principles
Description: This is my design principle page.
Template: analysis
---

# Design principles

I den här uppgiften ska vi analysera tre websidor utifrån ett design. Vikan jobba ensamma eller i grupp. Jag valde att jobba ensam.

# Urval

I kategorin personsidor tänkte jag genast på matbloggar. Jag gjorde därför mitt urval genom att välja de tre första namngivna träffarna på google när jag sökte på matblogg: 
Jennes matblogg - https://www.jennysmatblogg.nu/
Catarina König - https://catarinakonig.elle.se/
Trines matblogg - https://trinesmatblogg.no/

# Metod
Jag lade in sidans adress i verktygen PageSpeed, https://pagespeed.web.dev/ samt i Lighthouse. Från resultatet samlade jag in och analyserade den data som blev tillgänglig.

Jag började med färganalys och som stöd använde jag https://www.ginifab.com/feeds/pms/color_name_in_image.php för att identifiera färgerna och sedan kunna lägga in dem i ett färghjul - https://color.adobe.com/create/color-wheel. 

Några metoder som jag använde mig av för att analysera: 
https://dbwebb.se/guide/design-med-html5-och-css3/design - DBWEBB intern resurs
https://www.youtube.com/playlist?list=PLKtP9l5q3ce-oz7aoBkk-oEn4xzGbtqxU - design - principer och element
https://dbwebb.se/uppgift/tillganglighet-med-google-lighthouse - Lighthouse
https://www.ginifab.com/feeds/pms/color_name_in_image.php - what color is this?
https://color.adobe.com/create/color-wheel - Adobe color wheel.
https://www.toptal.com/designers/colorfilter/ - colorbild web page filter

# Resultat

Alla tre matbloggarna ligger runt 77-84 i tillgänglighet enligt Lighthouse. De har liknande diskret användning av färger och fokuserar på innehållet - att lyfta fram tilltalande bilder på mat och livsstil. Min favorit var den norska sidan, Trines, som jag upplevde som lättast att navigera. 

# Analys
## [Jennys matblogg ](https://www.jennysmatblogg.nu/): 
![Jennys](%assets_url%/img/design/jennys.jpg) {.img-control} Screenshot<br>
<br>

Webbplatsen handlar om mat - recept, reseskildringar med fokus på mat, tips, matsedlar mm. Personen bakom bloggen skriver också böcker som säljs via sidans shop. 

Jennes matblogg använder en diskret lila skala med närliggande färger med olika styrka. Även de grå nyanserna har en svag lila ton. 

<table style="border-spacing: 4px; border-collapse: separate">
<tr>
<td style="height: 50px; width: 50px; background-color: #c2bbdc">
<td style="height: 50px; width: 50px; background-color: #f0eff3">
<td style="height: 50px; width: 50px; background-color: #635b82">
<td style="height: 50px; width: 50px; background-color: #f9f9f9">
</tr>
</table>

Jag upplever sidan som övervägande vacker och stilren, med behagliga proportioner mellan sidebaren till höger och huvudelementet till vänster (2 + 1-proportioner). Vid närmare titt dyker det upp ett antal mindre "buggar" som drar ner uttrycket en del. Till exempel försvinner scrollbaren från veckomatsedlarna om man inte aktivt hovrar med musen över elementet - i kombination med att den understa veckan ser halvt avklippt ut gör det att elementet ser ofärdigt ut. Under senaste inlägget och veckomatsedel ligger ett trasigt annonselement - texten "annons" driver ut i marginalen "negative space" till höger och ingen annons har laddats när jag tittar på sidan, så flödet på sidan störs av stora, tomma block som reserverar plats för annonser.

Lighthouse: 
Sidan får 84/100 på tillgänglighet av Lighthouse. Bilderna saknar alt-attribut, länkar saknar tydliga namn, kontrasten är för låg och tabindex + heading element har för höga värden eller fel ordning. 

Färgblindhet: 
Jag ser inga stora problem när jag kör sidan genom färgfilter. 

## [Catarina König](https://catarinakonig.elle.se/):
![Catarinas](%assets_url%/img/design/catarinas.jpg) {.img-control} Screenshot<br>
<br>

Ytterligare en blogg om mat - den här gången under paraply från magasinet ELLE. Sidan är nästan totalt färglös - minimalistiskt vit med svart text och en extremt diskret grön färgton som färgar stjärnorna man kan sätta på recepten. 

<table style="border-spacing: 4px; border-collapse: separate">
<tr>
<td style="height: 50px; width: 50px; background-color: #d0dfd8">
<td style="height: 50px; width: 50px; background-color: #f0f0f0">
<td style="height: 50px; width: 50px; background-color: #7c7c7c">
<td style="height: 50px; width: 50px; background-color: #ffffff">
</tr>
</table>

Jag upplever sidan som minimalistisk inledningsvis - man möts av en stor bild på en kvinna som avnjuter någon elegant delikatess. Att scrolla längre ner avslöjar en serie stora bilder som ofta är för stora för att få plats på skärmen i sin helhet och inte skalar. Det finns ingen bra översikt om man inte går in via menyn längst upp till höger - vill man t.ex. hitta receptet på citronlax måste man söka manuellt på sidan eller chansa och scrolla ner. Även många av recepten tar så mycket plats att några av dem inte får plats att visas på en stor skärm på en gång utan att man måste zooma in/ut manuellt. Det blir mycket scrollande och jag som är normalfungerande upplever sidan som nästintill oanvändbar på en stationär dator. Dock vacker inledningsvis och gör ett bra första intryck. Använder man menyn och "vet vart man ska" så är det mindre problem. 

Den här webbsidan har distinkt olika design om man jämför huvudsidan med undersidor. Via menyn kan man t.ex. klicka på "kategorier" och hamnar då på en sida med en enkel navbar till vänster och en tre-kolumnslayout med recept till höger. Klickar man på recepten hamnar man dock tillabaka på huvudsidan, där receptet inte får plats på skärmen med mindre än att man manuellt zoomar ut. Jag måste zooma ut till 33% (!!!) för att kunna se hela receptet på citronlax inklusive bilden på rätten på en stor desktopskärm och då är texten inte läsbar. Alldeles för mycket scrollande. Antagligen är sidan optimerad för mobiler och desktop-versionen tillkom som en "afterthought".

Lighthouse: 
Lighthouse ger sidan 77/100 i tillgänglighet. Aria-attribut matchar inte sina rollar, knappar och länkar saknar namn, bilder saknar alt-attribut, och bakgrund/förgrund har inte tillräcklig kontrast. Det sista förvånar mig lite, eftersom sidan huvudsakligen är svart och vit - men länkar kan vara ljusblåa och svåra att se. Majoriteten av sidan och det huvudsakliga innehållet har ändå mycket tydlig text.

Färgbilndhet: 
Som en ren vit sida med svart text finns det ingenting att klaga på.

## [Trines](https://www.ginifab.com/feeds/pms/color_name_in_image.php):
![Trines](%assets_url%/img/design/trines.jpg) {.img-control} Screenshot<br>
<br>

En matblogg från Norge - den här gången med en blåskala. En top-bar i mörkblått och detaljer i en ljusare blå. Sidan har god balans med kolumner om tre element som visas samtidigt på varje rad.

<table style="border-spacing: 4px; border-collapse: separate">
<tr>
<td style="height: 50px; width: 50px; background-color: #323e56">
<td style="height: 50px; width: 50px; background-color: #e1e1e3">
<td style="height: 50px; width: 50px; background-color: #ffffff">
<td style="height: 50px; width: 50px; background-color: #c9d1da">
</tr>
</table>

Jag upplever den här sidan som den av de tre som är lättast att navigera. Den har en bra header som "följer med" när man scrollar ner, så man tappar aldrig bort sig på sidan. Färgschemat är diskret men trivsamt, ingenting ser trasigt ut och det finns tydliga länkar som man inte behöver trixa sig till via undermenyer. 

Bilderna är även på den här bloggen emellanåt lite för stora, men intrycket mildras något av att recepten åtminstone ligger i kolumner så att mer får plats på skärmen på en gång. 

Om man går in på recepten dyker det upp några roliga designelement ute till höger, t.ex. en "stikkord" med olika ord som är kopplade till den aktuella rätten och som man kan klicka på för att komma till andra liknande recept - orden har olika storlek och det lockar ögat (och muspekaren) till att klicka på de största.

Lighthouse:
Lighthouse ger 83/100 i tillgänglighet. Likt de andra sidorna finns anmärkningar på knappar, namngivning, elementordning för headers. Dessutom verkar man ha lagt in user-scalable="no" i meta-name="viewport".

Färgblindhet: 
Inga särskilda svårigheter.

## [Annas](http://www.student.bth.se/~anbx22/dbwebb-kurser/design/me/portfolio):
![Annas](%assets_url%/img/design/annasold.jpg) {.img-control} Screenshot<br>
<br>

Jag tittade också på min egen hemsida innan jag gjorde förbättringarna till kursmoment 6. Färgerna valde jag ursprungligen som ett mer eller mindre slumpmässigt tri-frägschema. Jag snurrade på Adobe-hjulet tills jag hittade något som inte såg anstötligt ut. Det var ett experiement och i efterhand tycker jag inte att det var så jättelyckat. Det blev för många starka färger som inte har någon koppling till innehållet.

<table style="border-spacing: 4px; border-collapse: separate">
<tr>
<td style="height: 50px; width: 50px; background-color: #a93c1d">
<td style="height: 50px; width: 50px; background-color: #feffff">
<td style="height: 50px; width: 50px; background-color: #95b2a6">
<td style="height: 50px; width: 50px; background-color: #e4926c">
</tr>
</table>

Rent designmässigt är jag inte nöjd med sidan. När jag tittar på den störs jag av kamperna mot Markdown, elementen som jag inte lyckades få full kontroll över och bildtexternas position.

Lighthouse gav mig ändå nästan tummen upp med 92 i accesibility innan trimningar! Det känner jag mig nöjd med trots allt. Synpunkterna jag får från Lighthouse är att html-elementet saknar ett lang-attribut, länkar saknar utskiljbara namn och en del element har tabindex med högre värde än noll. Det känns absolut görbart att peta upp 92 till 100.

# Referenser

Lighthouse https://dbwebb.se/uppgift/tillganglighet-med-google-lighthouse

# Övrigt

Författare: Anna Blixt
