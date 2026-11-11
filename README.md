# Zotte Familie Quizzes

Een gratis quiz-app in gewone HTML, CSS en JavaScript. Er is geen buildstap of account nodig. Zotte Familie Quizzes bewaart meerdere quizconcepten in een quizbibliotheek en bevat een starterquiz met 50 makkelijke vragen uit verschillende thema's. Vraagtypen: meerkeuze, waar/niet waar, jaartallen aanwijzen op een tijdlijn, open antwoord, meerdere juiste antwoorden en peilingen. Spelers kiezen bij het deelnemen een avatar en naam.

## Starten

Open `index.html` in je browser of start een statische webserver in deze map. De quizmaster houdt de pagina open tijdens het spel. De quizvragen worden automatisch lokaal in de browser van de quizmaster bewaard.

## Apart publiceren op GitHub Pages

De `index.html` in de hoofdmap van de volledige werkmap hoort bij Bright House Energy. Overschrijf die niet met de quiz. De workflow `.github/workflows/deploy-quiz-app.yml` publiceert alleen de map `quiz-app/` en laat de hoofdsite ongemoeid.

Upload de werkmapstructuur naar de GitHub-repository, inclusief `quiz-app/` en `.github/workflows/deploy-quiz-app.yml`. Kies daarna in **Settings → Pages** bij **Source** voor **GitHub Actions**. Voor de repository `aidenboyy/quiz` wordt de quizsite `https://aidenboyy.github.io/quiz/`.

Als je geen eigen domein hebt, maak **Custom domain** leeg in **Settings → Pages** en verwijder een eventueel `CNAME`-bestand uit de hoofdmap van de GitHub-repository.

## Deelnemers laten meedoen

De quizmaster maakt of bewerkt de quiz in de aparte Quiz maken-studio, start het spel en deelt de QR-code met de deelnemers. De pagina moet geopend zijn via een adres dat ook op hun telefoon bereikbaar is. Een `localhost`-adres of een `file://`-bestand werkt niet voor deelnemers op andere apparaten. Voor een klaslokaal kunnen alle apparaten dezelfde bereikbare website op het lokale netwerk gebruiken; voor spelers buiten dat netwerk moet de app op een publiek bereikbare HTTPS-website staan.

De verbinding tussen browsers gebruikt PeerJS en vereist internettoegang tot de PeerJS-signaleringsdienst. De QR-code wordt in de browser aangemaakt. Quizinhoud staat tijdens een spel in het geheugen van de quizmaster; sluit die pagina niet voordat het spel afgelopen is.

## Grenzen van deze eerste versie

- De zes tekens van de spelcode kunnen ook handmatig ingevoerd worden.
- Tijdlijnantwoorden krijgen punten als ze binnen 2,5% van het getoonde jaartalbereik liggen.
- Quizzen worden alleen lokaal in de browser van de maker opgeslagen en zijn niet automatisch tussen apparaten gesynchroniseerd.
- De quizmasterpagina moet open blijven. Er is geen centrale database of accountsysteem.