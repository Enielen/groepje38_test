# Introductie

Dit is de GitHub repository voor het thermodynamica deel van IP2. De bedoeling is dat je deze repository kloont en je vervolgens zelf een 'website' bouwt op basis van jouw werk. 

Per groepje volgt eentje de onderstaande stappen waarna de anderen uitgenodigd worden om bij te dragen aan deze repository.


## Klonen en opstellen van je eigen repository
Volg onderstaande instructie om je eigen repository op te stellen.

1. Ga naar de [repository](https://github.com/Contemporary-Physicslab/thermolab)
2. Klik op de groene knop `code` en kopier de url.
3. Open VSC en open een terminal (via `ctrl + ~` of via `view` $\rightarrow$ `terminal`).

```{note} Gebruik van de terminal
Je bent waarschijnlijk gewend om met een grafische interface (en je muis) te werken: Je klikt naar de locatie waar je heen wilt. In de terminal werk je met commando's. Navigeren door de terminal doe je met `cd <folder>` (waarbij `<folder>` de folder is waar je naartoe wilt gaan). 

Met `cd ..` ga je een folder omhoog. Met `ls` zie je de inhoud van de folder waar je in zit. Met mkdir `<folder>` maak je een nieuwe folder aan (waarbij `<folder>` de naam is van de nieuwe folder). Met rmdir `<folder>` verwijder je een lege folder (waarbij `<folder>` de naam is van de folder die je wilt verwijderen). 

Met `rm <file>` verwijder je een bestand (waarbij `<file>` de naam is van het bestand dat je wilt verwijderen). 

Met `code .` open je de huidige folder in VSC.
```

4. Navigeer in de terminal naar de locatie waar je je repository wilt opslaan (bijvoorbeeld `cd Documents/studie/jaar 1/IP2/`). Maak een nieuwe folder aan met `mkdir Project` en ga naar deze folder met `cd Project`.
5. Typ in de terminal `git clone <url>` (waarbij `<url>` de url is die je gekopieerd hebt) en druk op enter.

Nu worden alle bestanden van de repository gedownload naar je computer, maar deze zijn nog steeds gelinkt aan de originele repository (dus als je nu iets pusht, komt het in de originele repository terecht - dat mag echter niet want je hebt geen schrijfrechten). We moeten dus de link met de originele repository verbreken en een nieuwe repository aanmaken.

6. Open de folder in VSC (via `file` $\rightarrow$ `open folder`).
7. Open de terminal en typ `git remote remove origin` (om de link met de originele repository te verbreken).

Je kunt zowel via de terminal een nieuwe repository aanmaken als via de website van GitHub. Hieronder staat de methode via de website van GitHub beschreven. Ga naar [GitHub](https://github.com/) en doorloop onderstaande stap.

8. Maak een nieuwe repository aan op GitHub (via de `+` rechtsboven in je scherm en dan `new repository`).  
9. Kies een geschikte naam voor je repository (dit zal ook deel uitmaken van je URL!) en kies de optie `public`.
10. Ga in je repository naar `settings` en in het linkermenu naar `Pages` en kies `Github actions`
11. Klik op `code` en klik op het `gear-icon` (naast **About**) aan de rechterkant van de pagina.
12. Vink het vakje **Use your GitHub Pages website** aan.
13. Kopier de url van je nieuwe repository (deze heb je zo dadelijk nodig).

We hebben nu een nieuwe repository aangemaakt, maar deze is nog leeg. We moeten nu de bestanden die we gedownload hebben naar deze nieuwe repository pushen.

14. Ga terug naar VSC.
15. Typ in de terminal `git remote add origin <url>` (waarbij `<url>` de url is van je nieuwe repository).

Nu zijn de bestanden op je computer gelinkt aan je nieuwe repository, maar staan ze nog niet in je nieuwe repository. We moeten ze nu pushen.

16. Typ in de terminal `git push -u origin main` (om de wijzigingen naar je nieuwe repository te pushen).

Als je nu naar je nieuwe repository op GitHub gaat en de pagina ververst (via `F5` of via de `reload` knop in je browser), zie je dat alle bestanden zijn geupload. Je kunt nu ook de output zien op je eigen GitHub website! Klik daarvoor de link die rechts staat onder `code` $\rightarrow$ onder **About**.


## Je partner(s) uitnodigen
Bij IP2 werk je in tweetallen of drietallen. Je kunt je partner(s) uitnodigen om mee te werken aan jouw repository. Ga daarvoor naar je nieuwe repository op GitHub en doorloop onderstaande stappen.

1. Ga naar je nieuwe repository op GitHub.
2. Klik op `settings` (rechtsboven in je scherm).
3. Klik in het linkermenu op `manage access`.
4. Klik op de groene knop `invite a collaborator`.
5. Typ de gebruikersnaam van je partner(s) en klik op `add <username> to this repository` (waarbij `<username>` de gebruikersnaam is van je partner).

Als partner krijg je een mailtje met een uitnodiging om mee te werken aan de repository. Als je deze accepteert, kun je allebei wijzigingen aanbrengen in de repository.

## Je eerste wijzigingen doorvoeren
Je hebt nu een eigen repository met alle bestanden die nodig zijn om een website te bouwen. Je kunt nu zelf aan de slag om de inhoud van de website aan te passen. Belangrijkste is om eerst even de URL aan te passen in het hoofdbestand.

1. Open de `myst.yml` file in VSC. Daar zie je op twee plekken een URL naar github. Pas deze URL aan naar de URL van je eigen repository. 
2. Je kunt nu de repository bijwerken via de terminal, een andere optie is links in VSC te kliken op het `source control` icoon (het derde icoon van boven, dat eruit ziet als een vork met drie punten). Daar geef je een samenvatting van je wijzigingen en klik je op het vinkje (bovenaan) om de wijzigingen toe te voegen. Daarna klik je op de drie puntjes (bovenaan) en kies je `push` om de wijzigingen naar je repository te pushen.

```{warning} Let op
Nu anderen ook toegang hebben tot je repository, is het belangrijk dat je regelmatig kijkt of er wijzigingen zijn doorgevoerd. Dit doe je door een `pull` uit te voeren (via de drie puntjes bovenaan in het `source control` menu en dan `pull` te kiezen). Als je dit niet doet, kan het zijn dat je wijzigingen overschreven worden door die van een ander. 

Dus de volgende workflow is handig:
Als je start met werken: eerst een `pull` uitvoeren. Daarna je wijzigingen doorvoeren en deze `committen` en `pushen`.

Eventuele conflicten die ontstaan door gelijktijdig werken, kun je het systeem 'redelijk eenvoudig' oplossen.
```


```{warning} Pas op
Hieronder nog niet verwerkt
```



12. Ga terug naar VSC en open het bestand `.github/workflows/gh-pages.yml`.
13
. Vervang in dit bestand de regel `repository: Contemporary-Physicslab/thermolab` door `repository: <your-username>/<your-repo>` (waarbij `<your-username>` je GitHub gebruikersnaam is en `<your-repo>` de naam van je nieuwe repository).
13. Sla het bestand op (via `ctrl + s` of via `file` $\rightarrow$ `save`).
14. Open de terminal en typ `git add .` (om alle wijzigingen toe te voegen).
15. Typ `git commit -m "Initial commit"` (om de wijzigingen te committen).
16. Typ `git branch -M main` (om de hoofdbranch `main` te noemen).
17. Typ `git remote add origin <url>` (waarbij `<url>` de url is van je nieuwe repository).
18. Typ `git push -u origin main` (om de wijzigingen naar je nieuwe repository te pushen).
19. Ga naar je nieuwe repository op GitHub en ververs de pagina (via `F5` of via de `reload` knop in je browser).


23. Wacht tot alle cirkels groen zijn (dit kan een paar minuten duren, ververs de pagina eventueel met `F5`).

Het boek is nu gedeployed en kan bekeken worden via de url die je vindt onder `code` $\rightarrow$ onder **About**.

```{figure} ../Figures/rerunjobs.PNG
---
name: fig_rerun
width: 70%
---
Once the book has been deploy, all cirkels will be green.
```
