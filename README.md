# Världsnyheter på karta

En fristående HTML-sida som hämtar geotaggade nyheter live från GDELT och visar dem på en karta med kategoriikoner.

## Publicera på GitHub Pages (5 minuter)

1. **Skapa ett nytt repo**
   Gå till https://github.com/new, ge det valfritt namn (t.ex. `world-news-map`), välj Public, klicka "Create repository".

2. **Ladda upp filerna**
   På repots sida, klicka "Add file" → "Upload files". Dra in `index.html` och `.nojekyll` från den här mappen. Klicka "Commit changes".
   (`.nojekyll` är tom och behövs bara för att GitHub inte ska försöka Jekyll-processa sidan — ofarligt att ha med.)

3. **Aktivera GitHub Pages**
   Gå till repots **Settings** → **Pages** (i vänstermenyn).
   Under "Build and deployment" → "Source", välj **Deploy from a branch**.
   Under "Branch", välj **main** och mappen **/ (root)**. Klicka **Save**.

4. **Vänta ~1 minut**
   GitHub bygger sidan. Uppdatera Pages-sidan tills du ser en grön ruta med länken, i formatet:
   `https://ditt-användarnamn.github.io/world-news-map/`

5. **Öppna länken**
   Öppna den i valfri webbläsare (mobil eller dator) — den körs nu som en riktig webbsida med full nätverksåtkomst, ingen sandlåda.

## Uppdatera sidan senare

Redigera `index.html` direkt i GitHub (pennikonen på filen i repot) eller ladda upp en ny version via samma "Upload files"-flöde. Ändringar syns på den publicerade sidan inom någon minut.

## Anpassa data/beteende

Öppna `index.html` och leta upp dessa konstanter högst upp i `<script>`-taggen:

- `CATEGORIES` — vilka nyckelord/kategorier som söks och visas
- `TIMESPAN` — hur långt tillbaka i tiden som söks (t.ex. `'1h'`, `'6h'`, `'24h'`)
- `MAX_TOTAL_POINTS` — max antal nålar som ritas ut
- `AUTO_REFRESH_MINUTES` — hur ofta auto-uppdatering (om påslagen) hämtar ny data
