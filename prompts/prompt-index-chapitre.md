# Prompt de référence — Page d'accueil de chapitre (`index.html`)

Guide de référence pour la création des pages `index.html` dans chaque dossier `chNN/`.

---

## Philosophie générale

### Rôle de la page

La page `index.html` est le **portail d'entrée** du chapitre : un sommaire visuel qui regroupe en un seul endroit toutes les ressources disponibles (cours, exercices, fiche, simulation, QCM, DS…).

L'élève qui arrive sur un chapitre voit :
1. **Le titre et le contexte** (numéro, niveau, matière, domaine)
2. **Les objectifs pédagogiques**
3. **Les ressources organisées par usage** (découvrir / s'entraîner / s'évaluer)
4. **La navigation chapitre précédent ↔ suivant**

### Différence avec les pages sommaires (`maths-2nde-mama.html`, `pc-1ere-iccer.html`, etc.)

| Page | Périmètre | Navigation |
|---|---|---|
| Sommaire matière (`maths-2nde-mama.html`) | Tous les chapitres d'une classe | Liste plate avec liens |
| **Page chapitre (`index.html`)** | **Un seul chapitre** | **Cartes par type de ressource** |

L'`index.html` est l'« anti-chambre » du chapitre : on y choisit quoi faire (apprendre, s'entraîner, s'évaluer).

---

## Structure d'une page index

### Sections (dans cet ordre)

1. **En-tête** : lien retour vers le sommaire de la matière
2. **Hero** : numéro de chapitre, titre, sous-titre, compteur de ressources
3. **Objectifs** : reprise des objectifs du chapitre (extraits de `lecon.html`)
4. **Section « Découvrir et apprendre »** : activité, cours, fiche, simulation
5. **Section « S'entraîner »** : exercices, exercices-capacités
6. **Section « S'évaluer »** : QCM, interrogation, DS
7. **Footer nav** : chapitre précédent ← → chapitre suivant

### Cartes de ressources

Chaque ressource est une carte cliquable :
- **Icône** (emoji) en haut
- **Titre** en couleur thème
- **Description courte** (1 ligne)
- **Tag** indiquant la durée ou le type

Une carte « cours » est marquée `featured` (bordure et liseré) car c'est le contenu central.

| Ressource | Fichier | Icône | Description type | Tag |
|---|---|---|---|---|
| Activité de découverte | `activite.html` | 🧭 | Situation-problème guidée pour aborder la notion par un cas concret. | ~30 min |
| Cours | `lecon.html` | 📘 | Définitions, propriétés, méthodes et exemples résolus. | Référence (featured) |
| Fiche de révision | `fiche.html` | 📑 | Mémo synthétique : formules clés, méthodes, à imprimer. | ~5 min |
| Simulation interactive | `simulation.html` | 🔬 | Manipulation d'un modèle interactif lié au chapitre. | Interactif |
| Exercices | `exercices.html` | ✏️ | Exercices différenciés (socle, standard, approfondissement) avec corrections. | 3 niveaux |
| Exercices par capacités | `exercices-capacites.html` | 🎯 | Exercices organisés selon les capacités du programme officiel. | Programme |
| QCM interactif | `qcm.html` | ✅ | Auto-évaluation interactive avec correction automatique et score. | ~10 min |
| Interrogation | `interro.html` | 📝 | Évaluation courte chronométrée, barème /20. | ~15 min |
| Devoir surveillé | `ds.html` | 🎓 | Évaluation complète avec barème détaillé et correction. | 1 h |

**Règle :** ne lister que les ressources réellement présentes dans le dossier du chapitre. Une carte qui pointe vers un fichier inexistant produit un 404.

---

## Spécifications techniques

### Template HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>ChNN – Titre – Sommaire du chapitre</title>
<link rel="stylesheet" href="../../../styles.css">
<link rel="stylesheet" href="../../../print.css" media="print">
<style>
:root{--p:COULEUR;--p-bg:COULEUR-BG;--p-border:COULEUR-BORDER}

.ch-hero{
  background:linear-gradient(135deg,var(--p) 0%,#0a4f9c 100%);
  color:#fff;border-radius:14px;padding:32px 28px;margin:18px 0 28px;
  box-shadow:0 6px 20px rgba(0,0,0,.12)
}
/* … (styles complets dans les pages existantes, à dupliquer) … */
</style>
</head>
<body>
<div class="c">
<a href="../../../SOMMAIRE-MATIERE.html" class="nb">← Sommaire MATIERE</a>

<div class="ch-hero">
  <span class="ch-num">CHAPITRE NN</span>
  <h1>Titre du chapitre</h1>
  <p class="sub">Niveau | Matière | Domaine</p>
  <div class="meta"><span>X ressources</span></div>
</div>

<div class="ch-objectifs">
  <strong>Objectifs du chapitre</strong>
  <ul>
    <li>Objectif 1</li>
    <!-- 4 à 6 objectifs -->
  </ul>
</div>

<div class="ress-section">
  <h2>Découvrir et apprendre</h2>
  <div class="ress-grid">
    <!-- cartes activité, cours (featured), fiche, simulation -->
  </div>
</div>

<div class="ress-section">
  <h2>S'entraîner</h2>
  <div class="ress-grid">
    <!-- cartes exercices, exercices-capacités -->
  </div>
</div>

<div class="ress-section">
  <h2>S'évaluer</h2>
  <div class="ress-grid">
    <!-- cartes QCM, interro, DS -->
  </div>
</div>

<div class="ch-footer-nav">
  <a href="../chPP/index.html" class="nb">← Chapitre précédent : …</a>
  <a href="../chSS/index.html" class="nb">Chapitre suivant : … →</a>
</div>

</div>
<script src="../../../nav.js"></script>
</body>
</html>
```

### Couleur thème

Reprendre les variables CSS du chapitre (déjà définies dans `lecon.html`) :

| Section | `--p` | `--p-bg` | `--p-border` |
|---|---|---|---|
| `maths/seconde` | `#0056b3` | `#ebf5ff` | `#bee3f8` |
| `maths/premiere` ; `maths/terminale` ; `physique-chimie/premiere-iccer` ; `physique-chimie/terminale-iccer` ; `physique-chimie/premiere-gpt2` ; `physique-chimie/terminale-gpt2` | `#0969da` | `#dbeafe` | `#93c5fd` |
| `maths/lgt-terminale` | `#4f46e5` | `#eef2ff` | `#a5b4fc` |
| `maths/cap` | `#b45309` | `#fffbeb` | `#fde68a` |
| `physique-chimie/seconde` ; `physique-chimie/cap` | `#6f42c1` | `#f5f0ff` | `#c4b5fd` |
| `physique-chimie/premiere-era` ; `physique-chimie/terminale-era` | `#2da44e` | `#f0fff4` | `#86efac` |
| `physique-chimie/premiere-gpt4` ; `physique-chimie/terminale-gpt4` | `#7c3aed` | `#f5f3ff` | `#c4b5fd` |
| `physique-chimie/premiere-gpt6` | `#9333ea` | `#faf5ff` | `#d8b4fe` |
| `physique-chimie/terminale-gpt5` | `#059669` | `#ecfdf5` | `#86efac` |

### Lien retour selon la section

| Section | Lien retour |
|---|---|
| `maths/seconde` | `../../../maths-2nde-mama.html` |
| `maths/premiere` | `../../../maths-1ere-pro.html` |
| `maths/terminale` | `../../../maths-term-iccer.html` (ou `-erama` selon contexte) |
| `maths/lgt-terminale` | `../../../maths-lgt-terminale.html` |
| `maths/cap` | `../../../maths-cap.html` |
| `maths/bts` | `../../../maths-bts.html` |
| `physique-chimie/seconde` | `../../../pc-2nde-pro.html` |
| `physique-chimie/premiere-iccer` | `../../../pc-1ere-iccer.html` |
| `physique-chimie/premiere-era` | `../../../pc-1ere-erama.html` |
| `physique-chimie/premiere-gpt2/4/6` | `../../../pc-1ere-gpt2.html` (ou `-gpt4`, `-gpt6`) |
| `physique-chimie/terminale-iccer` | `../../../pc-term-iccer.html` |
| `physique-chimie/terminale-era` | `../../../pc-term-erama.html` |
| `physique-chimie/terminale-gpt2/4/5` | `../../../pc-term-gpt2.html` (ou `-gpt4`, `-gpt5`) |
| `physique-chimie/cap` | `../../../pc-cap.html` |

---

## Règles importantes

1. **Aucune ressource « fantôme »** : ne jamais lier vers un fichier inexistant. Détection automatique des fichiers présents recommandée.
2. **Compteur de ressources** : afficher le nombre réel de ressources disponibles (entre 4 et 9 selon les chapitres).
3. **Cours en `featured`** : la carte du cours porte la classe `featured` (bordure colorée + liseré).
4. **Footer nav** :
   - Si chapitre 01 : pas de « précédent », garder uniquement « suivant »
   - Si dernier chapitre : pas de « suivant », garder uniquement « précédent »
   - Le titre du chapitre voisin est affiché après les flèches (extrait du `lecon.html` voisin)
5. **Pas d'emoji dans le titre** : le titre est extrait tel quel du chapitre, sans décor ajouté
6. **`<title>` HTML** : suivre le format `ChNN – Titre – Sommaire du chapitre`
7. **Pas de timestamp `.maj`** : la page d'accueil est régénérée à chaque ajout de ressource — le timestamp serait constamment obsolète

---

## Génération automatisée

Le script `scripts/generate_chapter_index.py` automatise la création :

```bash
# Générer une page (sans écraser si elle existe)
python3 scripts/generate_chapter_index.py physique-chimie/premiere-gpt2/ch01

# Générer toutes les pages d'un dossier
python3 scripts/generate_chapter_index.py physique-chimie/premiere-gpt2

# Régénérer en écrasant
python3 scripts/generate_chapter_index.py --force physique-chimie/premiere-gpt2
```

Le script :
- Détecte les fichiers présents dans le dossier du chapitre
- Extrait le titre, le sous-titre, les objectifs et la couleur thème depuis `lecon.html`
- Détecte les chapitres voisins pour la nav prev/next
- N'inclut que les cartes de ressources qui correspondent à des fichiers réellement présents
- N'écrase pas un `index.html` existant sauf option `--force`

---

## Exemple complet

Voir `physique-chimie/seconde/ch02/index.html` (chapitre Grandeurs électriques) — modèle de référence.
