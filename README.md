# Mestská Farma Bratislava — nový web

Hugo + PaperMod theme + Decap CMS + GitHub Pages

---

## Prvotné nastavenie (raz)

### 1. Pridaj PaperMod theme
```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
git submodule update --init --recursive
```

### 2. Povoľ GitHub Pages
- Choď na GitHub → repozitár **Nova_farma** → **Settings** → **Pages**
- Source: **GitHub Actions**
- Ulož

### 3. Prvý commit a push
```bash
git add .
git commit -m "Prvý commit – nový web"
git push
```

GitHub Actions automaticky zostaví a nasadí stránku na:
`https://garubasro.github.io/Nova_farma/`

### 4. Presmerovanie domény (keď si pripravený)
V GitHub Pages nastaveniach zadaj Custom domain: `www.mestskafarmaba.sk`

---

## Pridávanie obsahu (bez technických znalostí)

Otvor v prehliadači: `https://www.mestskafarmaba.sk/admin/`

Prihlásiš sa cez GitHub účet a máš grafické rozhranie na:
- Písanie nových článkov (Zo záhrady)
- Správu zeleniny (čo je dostupné, ceny)
- Úpravu stránok O nás a Kontakt

---

## Štruktúra repozitára

```
content/
  posts/          ← články zo záhrady (blog)
  zelenina/       ← čo pestujeme (nie e-shop!)
  o-nas.md        ← o nás
  kontakt.md      ← kontaktná stránka
static/
  img/            ← sem skopíruj všetky obrázky zo starého webu
  admin/          ← Decap CMS (nepúšťaj sa do toho)
assets/css/extended/
  farma.css       ← vlastné štýly
layouts/          ← vlastné šablóny
```

---

## Obrázky

Všetky obrázky zo starého webu (`static/img/`) skopíruj do `static/img/` v tomto repozitári.
Cesty v článkoch ostávajú rovnaké: `/img/nazov-obrazku.jpg`
