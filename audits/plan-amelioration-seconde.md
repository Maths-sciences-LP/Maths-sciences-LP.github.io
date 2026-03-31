# Plan d'amelioration — Chapitres de Seconde

**Date** : 2026-03-17
**Derniere mise a jour** : 2026-04-02
**Perimetre** : maths/seconde (14 ch.) + physique-chimie/seconde (14 ch.)

---

## Etat des lieux

### Couverture des fichiers (28 chapitres)

| Section | Lecons | Exercices | DS | Total |
|---|---|---|---|---|
| Maths Seconde | 14/14 | 14/14 | 14/14 | 42/42 |
| PC Seconde | 14/14 | 14/14 | 14/14 | 42/42 |
| **Total** | **28/28** | **28/28** | **28/28** | **84/84** |

### Corrections : etat reel (verifie 2026-03-17)

**IMPORTANT** : L'audit precedent surestimait les corrections manquantes (comparaison sous-questions vs blocs `.corr`). La realite :

| Section | Boutons "Voir la correction" | Statut |
|---|---|---|
| PC Seconde exercices (ch01-ch14) | 12-26 par fichier | **Toutes presentes** |
| PC Seconde DS (ch01-ch14) | 7-10 par fichier, corr=parties | **Toutes presentes** |
| Maths Seconde exercices (ch01-ch14) | 12-15 par fichier | **Toutes presentes** |
| Maths Seconde DS (ch01-ch14) | 7-13 par fichier, corr=parties | **Toutes presentes** |

Les corrections sont **toutes redigees**. Le chiffre "517 manquantes" etait une erreur de comptage.

---

## Taches a realiser

### PRIORITE 1 — Problemes techniques (corrections rapides)

- [x] **PC ch04, ch05 lecon** — Labels `.label-def` verifies : deja correctement places a l'interieur des blocs ✅ (non-issue)
- [x] **PC ch01-ch14 lecon** — Titres `<title>` uniformises en UTF-8, entites HTML converties (6784 entites) ✅ 2026-04-02
- [x] **PC ch01-ch14 DS + exercices** — Entites HTML converties en UTF-8 sur tous les fichiers (9478 entites) ✅ 2026-04-02
- [x] **PC DS** — CSS inline verifie : classes `.partie`, `.pts`, `.comp-*` deja dans styles.css ✅ (non-issue)
- [x] **Maths Seconde ch07** — Badges `badge-niv badge-1/2/3` verifies : classes deja definies dans styles.css ✅ (non-issue)

### PRIORITE 2 — Ameliorations pedagogiques

- [x] **PC ch01-ch14 lecon** — Ajouter la classe `.situation` aux contextes professionnels existants ✅ 2026-03-31
- [x] **PC Seconde** — Diversifier les contextes pro : ajout sante, sport, energie, telecoms, quotidien ✅ 2026-03-31
- [x] **Maths ch02 lecon** — Section mode ajoutee, objectifs realignes sur le contenu reel, bloc `retenir` vers ch03 ✅ 2026-03-31
- [x] **Maths Seconde** — Sections "Erreurs frequentes" ajoutees dans les 8 chapitres qui en manquaient (ch03, ch09, ch10, ch11, ch12, ch13, ch14 + ch02) ✅ 2026-04-01

### PRIORITE 3 — Enrichissements

- [ ] **PC 1ere ICCER** — Ajouter des mini-exercices dans les lecons (actuellement 0 `.exo` dans les lecons)
- [ ] **PC Seconde** — Enrichir les situations professionnelles avec davantage de personnages/scenarios

---

## Organisation du travail

### Phase 1 : Corrections techniques (rapides, groupees)
1. Labels ch04/ch05 → deplacer a l'interieur des `.def`
2. Titres `<title>` uniformises sur les 14 lecons PC
3. Entites HTML → UTF-8 dans DS ch01-ch07
4. Badges de niveaux maths harmonises
5. Un seul commit

### Phase 2 : Ameliorations pedagogiques
1. Ajout `.situation` dans les 14 lecons PC Seconde
2. Completude de maths/seconde/ch02 (statistiques)
3. Diversification des contextes pro

### Phase 3 : Enrichissements
1. Mini-exercices lecons PC
2. Scenarios professionnels enrichis

---

## Corrections realisees

- **2026-03-31** : Ajout de blocs `.situation` sur 13 lecons PC Seconde (ch01-ch14, ch07 deja traite). Diversification des contextes professionnels : sante (audiologie, serums, oxymetre), sport (tapis de course, cycliste, salle de sport), energie (pompe a chaleur, thermostat, panneaux solaires), telecoms (fibre optique internet), quotidien (boisson, sudation, thermos). Maths ch01 : SVG ajoutés dans exercices et exercices-capacites. Maths ch02 : section mode ajoutee, objectifs realignes, bloc retenir vers ch03.
- **2026-04-01** : Sections "Erreurs frequentes" (blocs `.erreur-item`) ajoutees dans 7 lecons maths Seconde : ch03 (statistiques — mediane, IQR, etendue), ch09 (fonction affine — pente, sens de variation), ch10 (fonction carre — carre negatif, solutions), ch11 (figures planes — perimetre/aire, conversions), ch12 (Pythagore — hypotenuse, racine carree), ch13 (Thales — parallelisme, rapports, echelle), ch14 (solides — agrandissement, facteur 1/3). Total maths seconde : toutes les 14 lecons ont desormais une section erreurs frequentes.
- **2026-04-02** : Phase 1 — Conversion UTF-8 : 6784 entites dans lecons PC, 1772 dans DS ch01-ch07, 1492 dans DS ch08-ch14, 7214 dans exercices PC. Total ~17000 entites converties sur 42 fichiers PC Seconde. Titres `<title>` uniformises (13 lecons). Labels et CSS inline verifies : deja conformes. : ch03 (statistiques — mediane, IQR, etendue), ch09 (fonction affine — pente, sens de variation), ch10 (fonction carre — carre negatif, solutions), ch11 (figures planes — perimetre/aire, conversions), ch12 (Pythagore — hypotenuse, racine carree), ch13 (Thales — parallelisme, rapports, echelle), ch14 (solides — agrandissement, facteur 1/3). Total maths seconde : toutes les 14 lecons ont desormais une section erreurs frequentes.

---

## Suivi

| Phase | Statut | Date debut | Date fin |
|---|---|---|---|
| Phase 1 — Corrections techniques | Terminee | 2026-04-02 | 2026-04-02 |
| Phase 2 — Ameliorations pedagogiques | Terminee | 2026-03-31 | 2026-04-01 |
| Phase 3 — Enrichissements | A faire | — | — |
