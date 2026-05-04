# 🚀 Deploy OUH Guide til GitHub Pages

## Hvad du skal bruge
- En GitHub-konto (gratis på github.com)
- Git installeret på din PC (git-scm.com)

---

## Trin 1 – Opret GitHub repository

1. Gå til https://github.com/new
2. Repository name: `ouh-guide`
3. Sæt til **Public**
4. Klik **Create repository**

---

## Trin 2 – Upload filerne

Åbn terminal/PowerShell og kør:

```bash
# Gå til projektmappen (kopier filerne dertil først)
cd ouh-guide

git init
git add .
git commit -m "OUH Klinisk Guide"
git branch -M main
git remote add origin https://github.com/DIT-BRUGERNAVN/ouh-guide.git
git push -u origin main
```

(Erstat DIT-BRUGERNAVN med dit GitHub-brugernavn)

---

## Trin 3 – Aktiver GitHub Pages

1. Gå til dit repository på GitHub
2. Klik **Settings** → **Pages** (i venstre menu)
3. Under "Source": vælg **Deploy from a branch**
4. Branch: **main** / Folder: **/ (root)**
5. Klik **Save**

---

## Trin 4 – Din app er live! 🎉

Efter 1-2 minutter er appen tilgængelig på:

```
https://DIT-BRUGERNAVN.github.io/ouh-guide/
```

---

## Opdater appen fremover

Når du vil opdatere, kør bare:

```bash
git add .
git commit -m "Opdatering"
git push
```

GitHub Pages opdaterer automatisk inden for få minutter.

---

## Installer som app på telefon

**Android:**
Åbn linket i Chrome → Menu (⋮) → "Føj til startskærm"

**iPhone:**
Åbn linket i Safari → Del-ikon → "Føj til hjemmeskærm"

---

## Vigtigt om API-nøgle

Appen bruger Anthropic API (Claude). 
Nøglen håndteres automatisk af claude.ai's artifact-system når du kører den herfra.

Til selvstændig hosting skal du tilføje din API-nøgle i index.html:
Find linjen med `fetch('https://api.anthropic.com/v1/messages'` 
og tilføj i headers: `'x-api-key': 'DIN_NØGLE'`
