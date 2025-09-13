# Introductie

Dit is de GitHub repository voor het thermodynamica deel van IP2. De bedoeling is dat je deze repository kloont en je zelf een 'website' bouwt op basis van jouw werk. 

Per groepje volgt eentje de onderstaande stappen waarna de anderen uitgenodigd worden om bij te dragen aan deze repository.


## Klonen en opstellen van je eigen repository
Volg onderstaande instructie om je eigen repository op te stellen.

1. Ga naar de [repository](https://github.com/Contemporary-Physicslab/thermolab)
2. Klik op de groene knop `code` en kopier de url.
3. Open VSC en open een terminal (via `ctrl + ~` of via `view` $\rightarrow$ `terminal`).
4. Typ in de terminal `git clone <url>` (waarbij `<url>` de url is die je gekopieerd hebt).
5. Open de folder in VSC (via `file` $\rightarrow$ `open folder`).
6. Open de terminal en typ `git remote remove origin` (om de link met de originele repository te verbreken).
7. Maak een nieuwe repository aan op GitHub (via de `+` rechtsboven in je scherm en dan `new repository`).  
8. Kies een geschikte naam voor je repository (dit zal ook deel uitmaken van je URL!) en kies de optie `public`.
9. Ga in je repository naar `settings` en in het linkermenu naar `Pages` en kies `Github actions`
10. Kopier de url van je nieuwe repository (deze heb je zo dadelijk nodig).
11. Ga terug naar VSC en open het bestand `.github/workflows/gh-pages.yml`.
12. Vervang in dit bestand de regel `repository: Contemporary-Physicslab/thermolab` door `repository: <your-username>/<your-repo>` (waarbij `<your-username>` je GitHub gebruikersnaam is en `<your-repo>` de naam van je nieuwe repository).
13. Sla het bestand op (via `ctrl + s` of via `file` $\rightarrow$ `save`).
14. Open de terminal en typ `git add .` (om alle wijzigingen toe te voegen).
15. Typ `git commit -m "Initial commit"` (om de wijzigingen te committen).
16. Typ `git branch -M main` (om de hoofdbranch `main` te noemen).
17. Typ `git remote add origin <url>` (waarbij `<url>` de url is van je nieuwe repository).
18. Typ `git push -u origin main` (om de wijzigingen naar je nieuwe repository te pushen).
19. Ga naar je nieuwe repository op GitHub en ververs de pagina (via `F5` of via de `reload` knop in je browser).
20. Klik op `code` en klik op het `gear-icon` (naast **About**) aan de rechterkant van de pagina.
21. Vink het vakje **Use your GitHub Pages website** aan.
22. Ga naar `actions` in het bovenmenu, klik op de (rode) `initial commit` en klik op `re-run all jobs`.

23. Wacht tot alle cirkels groen zijn (dit kan een paar minuten duren, ververs de pagina eventueel met `F5`).

Het boek is nu gedeployed en kan bekeken worden via de url die je vindt onder `code` $\rightarrow$ onder **About**.

```{figure} ../Figures/rerunjobs.PNG
---
name: fig_rerun
width: 70%
---
Once the book has been deploy, all cirkels will be green.
```
