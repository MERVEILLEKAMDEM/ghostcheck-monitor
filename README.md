# 👻 Operation Ghost-Check

**Audit de risques IA & cybersécurité d'une infrastructure énergétique critique : de l'analyse de menaces au tableau de bord décisionnel.**

> Projet académique réalisé en équipe de 5 pendant une simulation « war room » de 9 heures, dans le cadre du MSc Cybersécurité & IA de l'**ESAIP** (mars 2026). L'entreprise **E-NRG** et l'attaque sont un **scénario fictif de simulation**.

## 🎯 Le scénario

Un attaquant utilise un **deepfake de la voix du PDG** pour ordonner un virement frauduleux de **5 millions d'euros**. L'attaque échoue de peu et révèle des failles opérationnelles, procédurales, techniques et réglementaires. Notre mission : cartographier toute la surface d'attaque liée à l'IA et livrer une **feuille de route de mitigation priorisée**.

## 🧭 Méthodologie

| Étape | Outil / cadre | Résultat |
|---|---|---|
| Analyse du contexte | **PESTLEO** (Politique, Économique, Social, Technologique, Juridique, Environnemental, Opérationnel) | 27 menaces réparties sur 7 facteurs |
| Analyse de chaque scénario | **QQOQCCP** (Qui, Quoi, Où, Quand, Pourquoi, Comment) | 7 scénarios d'attaque détaillés |
| Évaluation | **Matrice de criticité** : Probabilité (1-4) × Gravité (1-4), score maximal 16 | 7 risques notés et classés |
| Réponse | Mesures **préventives, protectrices, curatives** | 45 actions avec responsable et échéance |
| Restitution | Tableau de bord + pitch de 15 minutes | Priorités et plan d'action à 45 jours |

## 📊 Résultats

| ID | Risque | P | G | Score | Niveau |
|---|---|:-:|:-:|:-:|---|
| R1 | Fraude au deepfake vocal du PDG | 4 | 4 | **16** | 🔴 Critique |
| R7 | Approbation de virement par une seule personne | 4 | 4 | **16** | 🔴 Critique |
| R2 | Spear phishing généré par LLM | 4 | 3 | **12** | 🔴 Critique |
| R5 | Absence de protocole de réponse aux incidents IA | 4 | 3 | **12** | 🔴 Critique |
| R3 | Empoisonnement de données IA (OT/IT) | 3 | 4 | **12** | 🔴 Critique |
| R6 | Non-conformité RGPD / NIS2 | 3 | 3 | **9** | 🟠 Élevé |
| R4 | Attaque physique OT/IT sur l'infrastructure | 2 | 4 | **8** | 🟡 Moyen |

**7 risques identifiés, dont 5 critiques**, avec un score moyen de 12,1 / 16 et 45 actions de mitigation (dont 24 à priorité critique).

### Top 3 des priorités

1. **R1 + R7 (16/16)** : la double autorisation imposée au niveau de la plateforme bancaire (au-dessus de 10 k€) neutralise immédiatement la fraude au deepfake.
2. **R2 + R5 (12/16)** : filtrage e-mail comportemental par IA, clés MFA matérielles et playbook de réponse aux incidents IA sous 30 jours.
3. **R3 (12/16)** : contrôles d'intégrité des pipelines ML, segmentation OT/IT et sauvegardes versionnées des jeux d'entraînement.

### Conformité réglementaire

Le plan est construit autour des délais de notification **NIS2 (24 h, ANSSI)** et **RGPD (72 h, CNIL)**, avec des modèles de notification validés à l'avance et un responsable de notification doté d'une autorité pré-déléguée.

## 🖥️ Contenu du dépôt

| Fichier | Description |
|---|---|
| [`index.html`](index.html) | **Tableau de bord interactif** (HTML/CSS/JS, sans dépendance) : KPI, matrice de criticité, classement des risques, détail par risque et menaces par facteur PESTLEO. |
| [`risk_register.csv`](risk_register.csv) | Registre des risques (identifiant, source PESTLEO, probabilité, gravité, score, niveau, nombre d'actions). |

**Voir le tableau de bord en ligne** : https://merveillekamdem.github.io/ghostcheck-monitor/

## 👤 Mon rôle : « Hacker »

Rendre la menace crédible : transformer des concepts d'IA abstraits en scénarios d'attaque techniquement réalistes (clonage de voix à partir de quelques secondes d'audio, phishing généré par LLM, empoisonnement de données d'entraînement) et rédiger la partie **« Comment »** de chaque scénario QQOQCCP. Équipe de 5 : Hacker, Stratège, Communicant, Manager et Auditeur qualité.

## 🛠️ Compétences mobilisées

Analyse de risques (PESTLEO, QQOQCCP, matrice de criticité) · cybersécurité de l'IA · conformité NIS2 / RGPD · modélisation de données · tableaux de bord et data visualisation (Tableau, HTML/JS) · communication technique.

## ⚠️ Limites

Projet pédagogique : les données, l'entreprise E-NRG et l'incident sont fictifs. Le tableau de bord de ce dépôt est une reconstruction en HTML du tableau de bord Tableau présenté lors de la restitution.
