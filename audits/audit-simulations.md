# Audit Simulations Interactives

**Date** : 2026-03-16
**Périmètre** : dossier `simulations/` — 63 fichiers HTML

---

## Inventaire

### Simulations liées aux cours (7/63)

Ces simulations sont référencées depuis au moins une page de cours :

| Simulation | Lien depuis |
|---|---|
| `balance.html` | cours maths |
| `entrainement-ineq.html` | cours maths |
| `entrainement.html` | cours maths |
| `equations.html` | cours maths |
| `graphe-equation.html` | cours maths |
| `inegalite.html` | cours maths |
| `traceur.html` | cours maths |

### Simulations orphelines (56/63)

Ces simulations ne sont référencées dans **aucune page de cours**. Elles sont accessibles uniquement par URL directe ou depuis un éventuel index de simulations.

**Mathématiques** : `complexes.html`, `derivee.html`, `droite-affine.html`, `exp-log.html`, `figures-planes.html`, `fonction-machine.html`, `integrale.html`, `polynome3.html`, `probabilites.html`, `proportionnalite.html`, `pythagore.html`, `scalaire.html`, `solides.html`, `statistiques.html`, `stats-2var.html`, `suites.html`, `thales.html`, `trigonometrie.html`, `vecteurs.html`

**Physique** : `archimede.html`, `changement-etat.html`, `circuit-electrique.html`, `debit.html`, `dephasage.html`, `effet-joule.html`, `forces.html`, `moments.html`, `moteur.html`, `mouvement.html`, `ohm.html`, `ondes-em.html`, `pression.html`, `puissance.html`, `redressement.html`, `refraction.html`, `signal-alternatif.html`, `son-2nde.html`, `son.html`, `sources-lumineuses.html`, `transferts-thermiques.html`, `transformateur.html`, `transmission-info.html`, `vitesse-acceleration.html`

**Chimie** : `atome-couches.html`, `atome.html`, `chaleur.html`, `combustion.html`, `concentration.html`, `conductance-thermique.html`, `gaz.html`, `melangeur.html`, `modeles-atome.html`, `oxydoreduction.html`, `pile-electrochimique.html`, `rayonnement.html`, `serre.html`

---

## Problemes identifies

### 1. 89 % des simulations sont orphelines

**Gravité : HAUTE**

56 simulations sur 63 ne sont liées à aucune page de cours. Cela signifie :
- Les élèves ne peuvent pas y accéder facilement depuis leur cours
- Leur ancrage pédagogique n'est pas visible
- Elles risquent de ne jamais être utilisées

### 2. Pas d'index de simulations centralisé

Il n'existe pas de page listant toutes les simulations disponibles avec leur description et le chapitre associé. Seul un accès par URL directe est possible.

### 3. Autonomie des simulations

Les simulations doivent être autonomes (styles inline, pas de dépendance à styles.css ou nav.js). À vérifier fichier par fichier.

### 4. Correspondance programme non vérifiée

Chaque simulation devrait correspondre à une notion du programme officiel. Pour les 56 simulations orphelines, cette correspondance n'a pas été établie.

---

## Corrections realisees

- Aucune à ce stade.

---

## Ameliorations restantes

### Priorité haute
- [ ] Lier chaque simulation orpheline à la page de cours correspondante (lien dans lecon.html ou exercices.html)
- [ ] Créer un index des simulations (`simulations/index.html`) classé par matière et chapitre
- [ ] Vérifier l'ancrage pédagogique de chaque simulation (quelle notion du programme illustre-t-elle ?)

### Priorité moyenne
- [ ] Vérifier l'autonomie technique de chaque simulation (pas de dépendance externe cassée)
- [ ] Tester les simulations sur mobile (responsive)
- [ ] Ajouter une description pédagogique en en-tête de chaque simulation

### Priorité basse
- [ ] Identifier les chapitres sans simulation et proposer des simulations à créer
- [ ] Harmoniser le style visuel des simulations (couleurs, polices, mise en page)
- [ ] Ajouter des consignes d'utilisation pour les élèves sur chaque simulation
