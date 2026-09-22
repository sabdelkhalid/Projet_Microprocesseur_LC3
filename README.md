
---

## ⚙️ Partie 1 — Programmation Assembleur LC-3

Avant la conversion en assembleur, les routines ont été écrites en **C** pour valider la logique.  
Elles ont ensuite été traduites et testées en **assembleur LC-3**.

| Routine | Description | Difficulté principale |
|----------|--------------|------------------------|
| `strlen` | Calcule la longueur d'une chaîne. | Détection du caractère nul. |
| `index` | Trouve la première occurrence d’un caractère. | Gestion d’adresses mémoire. |
| `rindex` | Recherche la dernière occurrence d’un caractère. | Parcours inverse de la chaîne. |
| `strcmp` | Compare deux chaînes. | Longueurs différentes. |
| `strcpy` | Copie la chaîne source vers une destination. | Dépassements mémoire. |
| `strncpy` | Copie un nombre fixe de caractères. | Arrêt correct si chaîne courte. |

---

## ⚡ Partie 2 — Câblage des Circuits Logisim

### 🧠 Modules implémentés

#### 🔹 DecodeIR
- Extraction des champs `opcode`, registres, etc.  
- Utilisation de multiplexeurs et décodeurs.  
- Synchronisation avec ALU et NZP.

#### 🔹 ALU
- Exécute **ADD**, **AND**, **NOT**, **BSF**, **BSB**.  
- Gestion d’opérandes immédiats et registres.  
- Circuits additionnels pour scan de bits actifs.

#### 🔹 NZP
- Met à jour les indicateurs **N**, **Z**, **P** selon le résultat ALU.  
- Gestion fine des transitions d’état.

#### 🔹 Scan
- Implémente **BSF (Bit Scan Forward)** et **BSB (Bit Scan Backward)**.  
- Optimisation du circuit pour limiter la profondeur.

#### 🔹 WriteVal
- Sélectionne la bonne source de données (**ALU**, **Mémoire**, **PC**) via multiplexeurs.  
- Écrit le résultat dans le registre cible.

---

## 🚧 Défis rencontrés
- 🔸 Gestion rigoureuse des adresses mémoire  
- 🔸 Optimisation du câblage pour réduire la latence  
- 🔸 Synchronisation des signaux entre modules  

---

## ✅ Résultats
- 🧩 Version 1 : Modules DecodeIR, ALU, NZP, Scan terminés  
- ⚙️ Version 2 : WriteVal en cours d’intégration  
- 💾 Routines LC-3 testées et fonctionnelles  

---

## 🧰 Outils utilisés
| Outil | Utilisation |
|--------|--------------|
| **Logisim Evolution** | Simulation et conception du processeur |
| **LC3Edit / PennSim** | Programmation et exécution LC-3 |
| **Langage C** | Prototypage des routines avant conversion |

---

## 📘 Conclusion

Ce projet nous a permis de comprendre concrètement :
- la structure interne d’un processeur,
- le fonctionnement des modules logiques synchronisés,
- la relation entre **assembleur** et **architecture matérielle**.

Une expérience complète en **systèmes embarqués et architecture processeur** ⚡

---
