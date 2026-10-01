# 📄 Rapport de stage pré-ingénieur

**Modélisation d'un module d'extraction automatique de données pour documents administratifs : étude de cas Dolibarr**

![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white)
![Statut](https://img.shields.io/badge/statut-en_finalisation-0080ff?style=flat-square)
![Année](https://img.shields.io/badge/année_académique-2025--2026-0f172a?style=flat-square)

| | |
|---|---|
| **Auteur** | Henri Joël Fofack Alemdjou |
| **Formation** | Génie Informatique, École Nationale Supérieure Polytechnique de Yaoundé (Université de Yaoundé I) |
| **Structure d'accueil** | Novalitix |
| **Encadrement** | M. Brell Sanwouo, doctorant et CEO de Novalitix |
| **Code associé** | [Ophélia (DollPhelia)](https://github.com/ALEMDJOU/DollPhelia) |

---

## 🎯 Sujet

Les entreprises manipulent des documents très variés : factures, RIB, extraits Kbis, contrats, CV. En extraire les données reste difficile :

- les approches **à base de règles** sont rigides et cassent dès qu'un format change ;
- les **modèles d'IA génériques** perdent en précision sur les valeurs numériques et le contexte positionnel.

Ce rapport propose une **méthodologie hybride** qui combine :

1. l'**extraction par templates** (ancrage spatial, rapide et explicable) ;
2. la **reconnaissance d'entités nommées (NER)** ;
3. des **techniques de reconnaissance de motifs** (dates, montants, IBAN…) ;

le tout avec un **mécanisme d'apprentissage continu** qui s'adapte aux nouveaux formats sans réentraînement lourd. Le prototype est intégré comme module à l'ERP **Dolibarr**.

## 📊 Résultats annoncés dans le rapport

| Approche | Précision d'extraction |
|---|---:|
| Expressions régulières seules | 72 % |
| LLM générique (non fine-tuné) | 81 % |
| **Méthode hybride proposée** | **> 95 %** |

Évaluation sur un périmètre de 10 000 documents tests. Le prototype réduit la saisie manuelle de **80 %**.

## 📚 Plan du rapport

1. **Introduction générale** : contexte, problématique, objectifs
2. **Concepts généraux et état de l'art** : OCR, traitement intelligent de documents (IDP), LayoutLMv3, solutions du marché (AWS Textract, Azure Document Intelligence), comparaison des coûts
3. **Méthodologie** : analyse et conception UML (cas d'utilisation, classes, packages, séquences, workflow général)
4. **Références bibliographiques** et annexes

## 🗂️ Structure du dépôt

```
├── memoirthesis.tex          # Fichier principal (à compiler)
├── frontmatter/              # Page de titre, dédicace, déclaration, résumé, abstract, glossaire
├── chapters/
│   ├── chapter01/            # Introduction générale
│   ├── chapter03/            # Concepts généraux et état de l'art
│   ├── chapter04/            # Méthodologie + diagrammes UML (PDF)
│   ├── fig/                  # Figures de l'état de l'art
│   └── appendices/           # Annexes
├── biblio.bib                # Bibliographie
└── logos/                    # Logos institutionnels
```

## 🛠️ Compilation

Prérequis : une distribution LaTeX complète (TeX Live ou MiKTeX) avec les paquets `memoir`, `pgfornament`, `glossaries` et `import`.

```bash
git clone https://github.com/ALEMDJOU/RapportDeStageFofack.git
cd RapportDeStageFofack
pdflatex memoirthesis.tex
bibtex memoirthesis
pdflatex memoirthesis.tex
pdflatex memoirthesis.tex
```

Ou en une commande : `latexmk -pdf memoirthesis.tex`. Le projet peut aussi être importé tel quel sur [Overleaf](https://www.overleaf.com).

## 🙏 Crédits

Mise en page basée sur le modèle de thèse LaTeX pour l'ENSP de [Peterson Yuhala](https://github.com/Yuhala/latex-thesis), lui-même dérivé du modèle de l'Université de Bristol.

---

👤 **Henri Joël Fofack Alemdjou** · [Portfolio](https://portfoliofofackhenri.vercel.app/) · [LinkedIn](https://linkedin.com/in/henri-fofack-250b1b320) · [GitHub](https://github.com/ALEMDJOU)
