# Audit Programmes Officiels

**Date** : 2026-03-16
**Périmètre** : conformité du contenu avec les programmes Bac Pro, couverture des chapitres

---

## Programmes de référence disponibles

| Fichier PDF | Contenu |
|---|---|
| `programme_bacpro_seconde_maths_-_2019.pdf` | Programme maths Seconde |
| `programme_bacpro_seconde_sciences_-_2019-2.pdf` | Programme sciences Seconde |
| `programme_bacpro_premiere_maths_-_2020 (1).pdf` | Programme maths Première |
| `programme_bacpro_premiere_maths_-_2020-2.pdf` | Programme maths Première (copie) |
| `programme_bacpro_premiere_sciences_-_2020-2.pdf` | Programme sciences Première |
| `programme_bacpro_terminale_maths_-_2020 (1).pdf` | Programme maths Terminale |
| `programme_bacpro_terminale_sciences_-_2020.pdf` | Programme sciences Terminale |
| `BTS_ProgrammeMathematiques.pdf` | Programme maths BTS |
| `tableau_programmes_bts.pdf` | Tableau programmes BTS |
| `grille-ccf-maths-physique.pdf` | Grille d'évaluation CCF |
| `liste_groupements_bac_pro_.xlsx` | Liste des groupements |

---

## Problemes identifies

### 1. Incohérence chapitres terminale ICCER

CLAUDE.md déclare **11 chapitres** (ch01-ch11) pour `physique-chimie/terminale-iccer`, mais seuls **8 chapitres** (ch01-ch08) existent. Deux hypothèses :
- Les chapitres ch09-ch11 n'ont pas encore été créés
- Le programme a été ajusté et CLAUDE.md n'a pas été mis à jour

**Action** : vérifier le programme officiel (`programme_bacpro_terminale_sciences_-_2020.pdf`) pour le groupement ICCER et confirmer le nombre de chapitres attendus.

### 2. Doublons dans les PDF

Deux fichiers semblent être des copies du même programme :
- `programme_bacpro_premiere_maths_-_2020 (1).pdf`
- `programme_bacpro_premiere_maths_-_2020-2.pdf`

**Action** : vérifier si ces fichiers sont identiques et supprimer le doublon.

### 3. Vérification du contenu par rapport aux capacités attendues

Aucun audit systématique n'a été réalisé pour vérifier que chaque chapitre couvre bien les **capacités attendues** listées dans le programme officiel. Un tel audit nécessiterait une comparaison chapitre par chapitre.

### 4. Nommage des fichiers PDF

Les noms de fichiers PDF contiennent des espaces, des parenthèses et des suffixes incohérents (`-2`, `(1)`). Cela complique les références et l'automatisation.

---

## Corrections realisees

- Aucune à ce stade.

---

## Ameliorations restantes

### Priorité haute
- [ ] Vérifier le programme terminale sciences groupement ICCER et créer les chapitres manquants si nécessaire
- [ ] Mettre à jour CLAUDE.md si le nombre de chapitres terminale-iccer est bien 8

### Priorité moyenne
- [ ] Réaliser un audit capacités attendues vs contenu des cours, chapitre par chapitre
- [ ] Supprimer les doublons PDF
- [ ] Renommer les fichiers PDF avec une convention cohérente (sans espaces, sans parenthèses)

### Priorité basse
- [ ] Ajouter un fichier `pdf/README.md` listant chaque PDF et son contenu
- [ ] Vérifier que les grilles CCF correspondent aux dernières circulaires
