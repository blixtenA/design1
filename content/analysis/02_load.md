---
Title: Load
Description: This is my load page.
Template: analysis
---

# Colors

I den här uppgiften ska vi analysera tre websidor utifrån ett laddningsperspektiv / prestanda. Vikan jobba ensamma eller i grupp. Jag valde att jobba ensam, dels eftersom jag sitter i en annan tidszon och dels eftersom jag fortfarande har tappat rösten - inga större möjligheter att bolla med någon den här veckan. 

# Urval

Jag valde att fortsätta med de tre sidorna jag analyserade med avseende på färg förra veckan. Det är intressant att följa samma sidor genom olika analyser. 
SubWay, Farley Mowat Public School och the Weather Network.

# Metod
Jag lade in sidans adress i verktygen PageSpeed, https://pagespeed.web.dev/ samt i Google Pagespeed. Från resultatet samlade jag in och analyserade den data som blev tillgänglig. Respektive resultat sparade jag i ett Excel-ark som finns bifogat under Resultat. 

Det jag uppfattar som en snabb webplats är generellt laddningstider under 2 sekunder - men det beror på sidans innehåll. Om jag besöker en site i stil med Pricerunner eller Tripcentral som jag vet ska samla information från många andra siter, accepterar jag en betydligt längre laddningstid än om jag ska kontrollera öppettiderna till en affär jag avser besöka. 

# Resultat

<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTZSV34Zlfg2Ug2o7oV1vv_b665naRm1PJvFH4llB-acyL6eJ4AAtaRc73C4K-ODWP8Cp_FJRM9HOeW/pubhtml?widget=true&amp;headers=false"></iframe>

Farley Mowat Public School fick den lägsta Performance-poängen i testet - 3 på mobil. Detta förvånade mig mycket då mobilversionen av siten är förhållandevis slimmad och fungerar relativt bra rent funktionellt jämfört med desktop-versionen - förutom att skolans Twitterflöde är inkluderat på ett sätt som gör att man "fastnar" i ett subfönster och scrollar på sidans Tweets istället för att komma längre ner på skolans huvudsida. 

Högst poäng på performance var en nära kapplöpning mellan the Weather Network och SubWay - båda hamnade i rött på mobilplattformen (25 / 21 poäng) och på gult för desktop (64 / 65 poäng). Jag noterar att The Weather Network visar många annonser och i sitens natur ligger behandling av väderdata, medan SubWay i större utsträckning visar upp eget innehåll. Som en subjektiv skiljedomare skulle jag ge pokalen till The Weather Network, som visserligen presterade jämförbart med SubWay, men gjorde det med en svårare mängd data att processa och fler externa hämtningar av bilder och annonser. 

# Analys

## [Farley Mowat Public School](https://farleymowatps.ocdsb.ca/):
![FMPS](%assets_url%/img/FWPS.JPG) {.img-control} Screenshot<br>
<br>

https://farleymowatps.ocdsb.ca/
https://farleymowatps.ocdsb.ca/our_school
https://farleymowatps.ocdsb.ca/parent_resources

Farley Mowar Public School presterade generellt dåligt i Page Speed-testerna, med samtliga värden i rött eller orange. Performance på 3 för mobila plattformen är en mycket låg poäng. Under noteringar på Performance i vertyget finns: 

Serve images in next-gen formats
Reduce unused JavaScript
Efficiently encode images

När jag visuellt inspekterar sidan noterar jag att många av bilderna är hämtade från externa källor och inte särskilt anpassade för att visas med god prestanda. Relativt mycket material hämtas externt - till exempel får man skolans Twitterfeed laddad. Både Twitterfeeden och slideshowen som dominerar startsidan är bildtunga. Den stora förbättringen av den här websidan ser ut att kunna komma ifrån att optimera bildvisning.

Sidan har en relativt lång laddningstid på över 3 sekunder och laddar resources på hela 56 MB i genomsnitt, med upp till 4,7 MB överfört. Utöver att se över bilderna kan det vara en god idé att se över vad som egentligen laddas på sidan och om det finns möjlighet att paketera laddningarna i mindre enheter som kan laddas vid förfrågan istället för automatiskt.

## [SubWay](https://order.subway.com/en-CA):
![SubWay](%assets_url%/img/SUBWAY.JPG) {.img-control} Screenshot<br>
<br>

https://order.subway.com/en-CA
https://order.subway.com/en-ca/locator
https://order.subway.com/en-ca/menunutrition/menu

SubWay prespterade relativt gott i mätningarna från Page Speed och skickade minst information - i genomsnitt mottogs endast 484 kb data. Sidan tog i snitt 7,5 sekunder på sig till Finish, med en Load på 1,71 - bäst i test. 

Page Speed ger följande förslag för siten: 

Serve images in next-gen formats
Properly size images
Efficiently encode images

Som för de båda andra siterna tycks bilderna vara det stora problemet och det som innehåller bäst förbättringspotential. Då SubWay framför allt marknadsför sina egna produkter torde företaget ha en hög grad av kontroll över innehållet och bilderna. Det finns inga synliga reklamsegment från externa källor. Jag noterar inga inbäddade flöden från företagets Facebook eller Twitter - koppling till social media ligger som enkla länkar i Footern. 

Jag ser inga stora förbättringsmöjligheter för den här siten vid en översiktlig analys. Emedan siten visar upp ett antal bilder, så är det sällan många bilder på en gång. 

Mobilsiten är mycket hanterlig att navigera och jag upplever inga prestandaproblem eller andra störningar när jag testar navigering. 

## [The Weather Network](https://www.theweathernetwork.com/ca/weather/ontario/ottawa?wx_auto_reload=): 
![FMPS](%assets_url%/img/TWN.JPG) {.img-control} Screenshot<br>
<br>

https://www.theweathernetwork.com/ca/weather/ontario/ottawa?wx_auto_reload=
https://www.theweathernetwork.com/ca/36-hour-weather-forecast/ontario/ottawa
https://www.theweathernetwork.com/ca/monthly/ontario/ottawa

The Weather Network presterade relativt gott i mätningarna från Page Speed. De tre laddningsmätningarna uppvisade väldigt olika resultat med avseende på laddningstid - från 702 millisekunder till 3,78 sekunder. Som användare upplevde jag att den stora skillnaden låg i vilka annonser som laddades. Sidan visar upp en rad reseannonser på högerkanten. Sidan har också en bakgrund som ändrar sig efter rådande väder - när screenshotten ovan togs var vädret vackert i verkligheten och bakgrunden visade fluffiga moln i en grå/blå skala. I skrivandet stund är det dock regnigt ute och bakgrunden på siten har ändrats till grå med regnstrimmor. 

Omdömena på Page Speed lämnar olika förslag för Mobil och Desktop:

Mobil: 
Reduce unused JavaScript
Serve images in next-gen formats
Efficiently encode images

Desktop:
Serve images in next-gen formats
Eliminate render-blocking resources
Reduce unused JavaScript

Högt på listorna kommer fix av bilderna och JavaScript. Jag noterar också under Accesibility att det ges en synpunkt på bakgrunden: "Background and foreground colors do not have a sufficient contrast ratio." Utöver att förbättra bilderna kodning och rensa bort JavaScript-kod som inte används, kan det hända att även bakgrunden skulle kunna förenklas och snabba upp laddning samt användbarhet. 

Jag noterar att bakgrunden är enfärgad på mobilen och att siten är relativt svårnavigerad på mobilen på grund av många reklamsegment som bryter upp navigeringen. 

# Referenser

Page Speed https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect

# Övrigt

Författare: Anna Blixt
