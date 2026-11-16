# Rapport TP Micro-332 — projet LaTeX (groupe 8)

## Importer dans Overleaf
1. Overleaf → **New Project** → **Upload Project** → choisir `rapport-micro332.zip`.
2. Compilateur : **pdfLaTeX** (réglage par défaut). Fichier principal : `main.tex`.

## Organisation
- `main.tex` : ordre des parties (chaque sujet commence sur une nouvelle page).
- `preambule.tex` : packages, mise en page, commandes du rapport.
- `sections/` : un fichier par partie (`sujet1.tex` … `sujet6.tex`, introduction, conclusion, références). Chacun peut éditer son sujet sans toucher aux autres.
- `figures/` : graphiques pgfplots et schémas TikZ, modifiables directement.
- `data/` : mesures du sujet 1 (`sujet1_epaisseur.dat`, `sujet1_contraste.dat`), lues par les graphiques.
- `photos/` : y déposer les photos et le logo (voir plus bas).

## Marqueurs rouges
- `\acompleter{...}` et `\averifier{...}` s'affichent en rouge gras dans le PDF. Chercher « acompleter » et « averifier » pour les retrouver.
- Pour le rendu final, décommenter `\versionfinaletrue` dans `main.tex` : tous les marqueurs disparaissent.

## Photos et logo
Déposer les fichiers dans `photos/` avec exactement ces noms ; ils s'affichent à la place des cadres rouges.

| Fichier | Sujet |
| --- | --- |
| `logo_epfl.pdf` (ou `.png`) | Page de garde |
| `s1_adhesion_avec_hmds.jpg`, `s1_adhesion_sans_hmds.jpg` | 1 |
| `s2_nlof_58s.jpg`, `s2_bicouche.jpg`, `s2_apres_liftoff.jpg` | 2 |
| `s3_optique_nlof.jpg`, `s3_meb_nlof.jpg`, `s3_meb_bicouche.jpg` | 3 |
| `s5_plaquette_gravee.jpg`, `s5_profil_dektak.png` | 5 |

Pour ajouter une photo : `\photo{photos/nom.jpg}{légende}{fig:label}` ou deux côte à côte avec `\photopaire{...}{...}{...}{...}{...}{...}`.

## Données du sujet 1
- Les moyennes de la feuille Excel étaient fausses (somme des 5 points divisée par 4). Les valeurs correctes sont dans `data/sujet1_epaisseur.dat`.
- Si une épaisseur initiale e0 change, mettre à jour le diviseur correspondant dans `figures/fig1_2_contraste.tex` (ex. `\thisrow{e2000}/1.8193`) ainsi que les tableaux 1.2 à 1.4.
- L'intensité de la lampe (3,11 mW/cm²) est définie une seule fois en haut de `figures/fig1_2_contraste.tex`.

## Longueur
Consigne : 4 pages maximum par sujet. Actuellement le sujet 1 fait 4 pages avec les cadres photo vides ; les vraies photos (5,5 cm de haut maximum) peuvent ajouter un peu de place.

## Rendu
PDF à envoyer à A. Sayah deux semaines après la dernière séance.
