# Web vfko.cz

Statický web pro GitHub Pages. Nepotřebuje žádný build. Stačí nahrát obsah této složky do kořene repozitáře.

## Stránky

| Soubor | Adresa |
|---|---|
| `index.html` | vfko.cz |
| `co-je-noveho/index.html` | vfko.cz/co-je-noveho/ |
| `zasady/index.html` | vfko.cz/zasady/ (tuto adresu má aplikace v `ZASADY_URL`) |
| `404.html` | stránka „nenalezeno“ (GitHub Pages ji použije sám) |

Styly jsou v `assets/styles.css`, písma v `assets/fonts`, obrázky v `assets/img`. Web nepoužívá cookies, měření ani externí zdroje.

## Zveřejnění na GitHub Pages

1. Nahrajte obsah složky do repozitáře, například `vfko-web`, do větve `main`.
2. V repozitáři otevřete **Settings → Pages**. V části **Source** zvolte `Deploy from a branch`, větev `main` a složku `/ (root)`.
3. Soubor `CNAME` už obsahuje `vfko.cz`.
4. U registrátora domény nastavte DNS:
   - `A` záznamy pro `vfko.cz`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`,
   - `CNAME` pro `www`: `<váš-github-účet>.github.io`.
5. Po ověření domény zapněte **Enforce HTTPS**.

Doporučuji ještě ověřit doménu v nastavení GitHub účtu (**Settings → Pages → Verified domains**). Nikdo jiný ji pak nebude moct připojit ke svému repozitáři.

## Před spuštěním doplnit

- Ve všech souborech nahraďte `GITHUB_UZIVATEL` vaším účtem na GitHubu. Jsou to odkazy na GitHub Releases.
- Žlutě zvýrazněné texty (třída `ph`) jsou místa k doplnění:
  - IČO a místo podnikání,
  - verze a datum vydání,
  - minimální verze macOS,
  - poskytovatel e-mailu a doby uložení v zásadách,
  - datum účinnosti zásad,
  - odkaz na návod k přenosu dat.
  
  Po doplnění odstraňte i obalující `<span class="ph">`.
- Stránka `/podminky/` (Licenční podmínky) zatím neexistuje. Odkaz v patičce do jejího vytvoření vede na stránku 404.
- Adresa `podpora@vfko.cz` musí fungovat ještě před spuštěním.

## Nová verze aplikace

V `co-je-noveho/index.html` je u prvního záznamu komentář s postupem:

1. Zkopírujte celý blok `<section class="release">`.
2. Vložte ho nad předchozí blok.
3. Změňte číslo verze, datum, `id` (např. `v1-0-3`) a seznam změn.

Na úvodní stránce v sekci Stažení upravte číslo verze a datum. V `sitemap.xml` není potřeba nic měnit.

## Obrázky

- `hero-aplikace.webp` a `historie-uhrady.webp` jsou snímky skutečné aplikace s ukázkovými daty, ve dvojnásobném rozlišení.
- `faktura-vyrez.webp` je výřez ukázkové faktury.
- `og.png` (1200 × 630 px) je obrázek pro sdílení odkazu.
- Favicony vznikly ze zjednodušené malé ikony podle brand manuálu.
