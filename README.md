# Rīga kustībā — GitHub Pages versija

Gatava HTML/CSS/JavaScript mājaslapa ar saglabātu tumšo/zaļo dizainu. Nav jāinstalē Node.js, npm vai citas pakotnes. Fonti, galvenais attēls un transporta dati ir iekļauti.

## Publicēšana GitHub Pages
1. Atarhivē ZIP savā datorā.
2. Izveido GitHub repozitoriju vai atver repozitoriju, kurā vēlies šo mājaslapu. Pirms esošu failu aizstāšanas saglabā iepriekšējo versiju.
3. Spied **Add file → Upload files**. Augšupielādē arhīva SATURU, saglabājot `assets` un `data` mapes. Augšupielādē atarhivētos failus, nevis ZIP. `index.html`, `style.css` un `app.js` jābūt repozitorija saknē.
4. Saglabā izmaiņas ar **Commit changes**.
5. Atver **Settings → Pages**. Sadaļā **Build and deployment** izvēlies **Deploy from a branch**, zaru **main** un mapi **/ (root)**. Spied **Save**.
6. Kad GitHub pabeidz publicēšanu, šajā sadaļā būs mājaslapas adrese, parasti `https://TAVS-LIETOTAJVARDS.github.io/REPOZITORIJA-NOSAUKUMS/`.

Oficiālā instrukcija: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

Ja datorā nav redzams `.nojekyll`, pārējie šīs vietnes faili joprojām ir izmantojami. Šis fails tikai izslēdz GitHub Jekyll apstrādi. Ja nepieciešams, izveido repozitorijā tukšu failu ar nosaukumu `.nojekyll`.

## Kas jāsaglabā kopā
- `index.html` — mājaslapas struktūra.
- `style.css` — viss vizuālais noformējums.
- `app.js` — pogu, meklēšanas un kartes darbība.
- `assets/tram-hero.png` — galvenais attēls.
- `assets/fonts/` — Manrope fonti (arī latviešu burti) un to licence.
- `data/` — 80 JSON faili ar maršrutiem un pārējiem datiem.

Visi iekšējie ceļi ir relatīvi. Lapa paredzēta darbam arī GitHub projekta apakšmapes adresē. Nav piesaistes ChatGPT vai Sites.

## Apskate datorā
Dizainu var apskatīt, atverot `index.html`. Pilnai datu ielādei nepieciešams HTTP serveris. Ja instalēts Python, atver termināli šajā mapē un izpildi:

```sh
python -m http.server 8000
```

Atver http://localhost:8000. GitHub Pages pats nodrošina serveri — publicētajai lapai Python nav vajadzīgs.

## Pārskatītās lietas
- Iekļauti lokāli fonti; nav vajadzīgs Google Fonts savienojums.
- Saglabāts galvenais attēls, krāsas, sadaļas un izkārtojuma stils.
- Nostiprināta garu nosaukumu un ļoti šauru ekrānu apstrāde.
- Novērsta veca maršruta atbildes kļūdas parādīšana pēc jaunāka maršruta izvēles.
- Aizsardzība pret nekorekti saglabātu favorītu vērtību pārlūkā.
- Pārbaudīta JavaScript sintakse, failu saites, lokālie fonti un datu failu esamība.
- Pilna vizuālā pārbaude reālā pārlūkā šajā vidē nebija pieejama.

## Saturs
Neoficiāls dizaina prototips, nevis pārvadātāja oficiālā vietne. Plānotie laiki no lietotāja pievienotās datu kopas. Karte ir ģeogrāfiska maršrutu shēma. Braucienu meklētājs meklē tiešos reisus bez pārsēšanās. Nav GPS reāllaika datu. Galvenais tramvaja attēls ir AI veidota ilustrācija.

Ārējās saites uz Rīgas satiksmi un OpenStreetMap atver attiecīgās vietnes. Tās nav vajadzīgas šīs lapas dizaina ielādei.
