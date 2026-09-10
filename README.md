Adam - hero.css
Jennifer - highlights.css
Alecia - schema.css
Samane - nav_footer.css, respons.css
Alla - nav_header.css

**Vad innebär semantisk HTML och varför har ni använt det på er eventsida?**

Semantisk HTML betyder att man använder HTML-taggar som beskriver vad innehållet på sidan är. Till exempel använder vi <header> för sidans början, <main> för huvudinnehållet och <footer> för information längst ner på sidan.
På vår eventsida har vi använt semantisk HTML för att göra sidan mer tydlig och lättare att förstå. Vi har till exempel <section> för olika delar av sidan och <article> för olika artister och höjdpunkter. Vi använder också <nav> för länkarna i footern.
Vi har använt semantisk HTML eftersom det gör koden mer strukturerad och det blir lättare för både användare och webbläsare att förstå hur sidan är uppbyggd och för att skärmläsare skall fungera korrekt.

**Hur fungerar arv i CSS? Ge ett exempel från er egen kod.**

Arv betyder att vissa CSS-egenskaper (t.ex. color, font-family) på en förälder förs vidare till barnen om barnen inte sätter egna värden.
I vår kod har vi använt arv genom att sätta ett typsnitt på body:
body {
font-family: 'Lucida Sans', sans-serif;
}

Eftersom nästan all text finns inuti body så får texten typsnittet automatiskt. Vi behöver alltså inte skriva font-family på alla olika delar av sidan.
Man kan också ändra det på ett speciellt element. Till exempel har vi .contact där vi använder Arial istället. Då gäller Arial bara för den delen.
Arv är bra eftersom man kan skriva mindre kod och få samma stil på flera delar av sidan.

**Vad är den största skillnaden mellan Flexbox och CSS Grid, och när ska man använda vilket verktyg? Motivera utifrån hur ni fördelade dem på er sida.**

Den största skillnaden mellan Flexbox och CSS Grid är att Flexbox passar bäst när man vill placera saker i en rad eller kolumn, medan Grid passar bättre när man vill göra ett rutnät med flera rader och kolumner.
På vår sida har vi använt Flexbox till exempel på höjdpunkterna. Där har vi flera kort bredvid varandra och använder:
.kort-rad {
display: flex;
flex-wrap: wrap;
justify-content: center;
gap: 3.55rem;
}

Vi använde Flexbox eftersom korten ska ligga bredvid varandra och kunna flytta ner på nästa rad när skärmen blir mindre.
Vi har använt CSS Grid till tidtabellen. Där har vi tre kolumner:
.tidtabell {
display: grid;
grid-template-columns: auto auto auto;
}

Grid passar bra här eftersom tidtabellen ska vara uppdelad i flera kolumner och rader.
Vi valde alltså Flexbox för att placera kort och Grid för att bygga upp tidtabellen. På mobilen ändras båda så att innehållet blir lättare att se.
