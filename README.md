# Jurnal Barber

Aplicație PWA personală pentru înregistrarea rapidă a tunsurilor, tips-urilor
și împărțirii banilor cu șeful. Fără cont, fără server — toate datele stau
doar pe telefonul tău (localStorage), iar aplicația funcționează offline
după prima încărcare.

## Structura proiectului

```
index.html      – ecranele aplicației (Azi / Istoric / Profil)
styles.css      – tot stilul vizual
app.js          – toată logica (date, calcul, salvare)
manifest.json   – configurația PWA (nume, iconițe, culoare)
sw.js           – service worker pentru funcționare offline
icons/          – iconițele aplicației
```

Nu există niciun backend. E doar un site static — orice găzduire statică
gratuită funcționează.

## Cum îl pui online (gratuit, fără cont de dezvoltator Apple)

Ai nevoie ca fișierele să fie servite prin **HTTPS** (obligatoriu pentru PWA
și pentru instalare pe iPhone). Cea mai simplă variantă:

### Opțiunea 1 — Cloudflare Pages (recomandat)
1. Creează un cont gratuit pe [pages.cloudflare.com](https://pages.cloudflare.com).
2. „Create a project” → „Direct upload” → trage tot folderul `barber-journal`.
3. Primești un link de tipul `https://jurnal-barber.pages.dev`.

### Opțiunea 2 — Netlify
1. Cont gratuit pe [netlify.com](https://netlify.com).
2. „Add new site” → „Deploy manually” → trage folderul `barber-journal`.
3. Primești un link `https://ceva.netlify.app`.

### Opțiunea 3 — GitHub Pages
1. Urcă fișierele într-un repo GitHub.
2. Settings → Pages → activează pentru branch-ul principal.
3. Primești un link `https://username.github.io/repo`.

Oricare din cele trei e suficient — nu ai nevoie de mai mult de unul.

## Cum îl instalezi pe iPhone (Home Screen)

1. Deschide linkul aplicației în **Safari** (obligatoriu Safari, nu Chrome).
2. Apasă butonul de **Share** (pătratul cu săgeata în sus).
3. Alege **„Add to Home Screen” / „Adaugă pe ecranul principal”**.
4. Apasă **Adaugă**.

Aplicația apare acum ca o iconiță normală, se deschide pe tot ecranul (fără
bara Safari) și funcționează offline după prima deschidere.

## Notă despre date

Datele sunt salvate doar în acest browser, pe acest telefon. Dacă ștergi
Safari/datele site-ului sau schimbi telefonul, le pierzi — de aceea, din
Profil → „Exportă datele (backup)” poți salva oricând o copie într-un
fișier `.json`, pe care o poți importa înapoi de pe orice telefon.
