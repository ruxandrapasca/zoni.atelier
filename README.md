# Zoni Atelier · Globuri 2026

Site-ul cu oferta de globuri. Se publică automat pe GitHub Pages, la https://zoniatelier.github.io, la fiecare modificare din repository.

## Structura

- `index.html` – pagina (design, coș, trimitere comandă). De obicei nu trebuie modificată.
- `produse.json` – colecțiile, globurile și prețurile.
- `poze/` – pozele globurilor și ale cutiilor.

## Cum adaugi un glob

1. Urcă poza în folderul `poze/` (pe GitHub: intri în `poze` → **Add file** → **Upload files**). Folosește un nume simplu, fără spații și diacritice, de ex. `reindeer.jpg` (merg și .png sau .webp).
2. Deschide `produse.json` → iconița de creion → în colecția dorită adaugă un rând în lista `globuri`:

   ```json
   { "nume": "Reindeer", "poza": "reindeer.jpg" },
   ```

3. **Commit changes**. În ~30 de secunde apare pe site.

## Cum ștergi un glob

Șterge rândul lui din `produse.json` (atenție la virgule: ultimul element dintr-o listă nu are virgulă după el). Poza din `poze/` poate rămâne sau o poți șterge.

## Cum schimbi o poză

Urcă poza nouă cu **alt nume** (ex. `fox-2.png`) și schimbă numele în `produse.json`. Cu un nume nou, browserele clienților nu mai arată poza veche din memorie.

## Cum schimbi un preț

În `produse.json`, la colecția respectivă, schimbă `"pret": 75`.

## Câmpuri opționale ale unei colecții

- `"nota"` – textul afișat sub titlu.
- `"notaPret"` – prețul afișat lângă notă, ex. `"+15 lei"`.
- `"pretPersonalizareNume": 15` – adaugă bifa „Personalizare cu nume” în coș.
- `"textPersonalizat": true` – adaugă câmpul de text personalizat în coș.
- Un glob fără `"poza"` apare ca „În curând”.

Prima poză din listă e afișată mare. Dacă o colecție are mai mult de 5 globuri, cele mici apar pe 4 coloane în loc de 3.
