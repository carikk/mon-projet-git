# 🧪 TP : Maîtriser Git et GitHub (CLI & IntelliJ IDEA)

## 🎯 Objectifs

- 📌 Comprendre les bases de Git et GitHub  
- 🗃️ Créer et gérer un dépôt distant  
- 🌿 Utiliser les branches, commits et fusions  
- 💻 Maîtriser Git en ligne de commande et avec un IDE (IntelliJ)

---

## 🧰 Prérequis

- 👤 [Avoir un compte GitHub](https://github.com)  
- ⚙️ [Installer Git](https://git-scm.com)  
- 🧠 Connaître les bases du terminal  
- 🛠️ [Installer IntelliJ IDEA](https://www.jetbrains.com/idea)

---

## 🔹 Partie 1 — Création du dépôt GitHub

1. Allez sur [GitHub](https://github.com) et connectez-vous  
2. Cliquez sur ➕ **New repository**  
3. Remplissez :
   - **Repository name** : `mon-projet-git`
   - **Description** : (optionnelle)
   - Visibilité : Public ou Private  
   - ✅ Cochez **Add a README file**
4. Cliquez sur **Create repository**
5. Copiez l'URL HTTPS :  
   `https://github.com/ton-utilisateur/mon-projet-git.git`

```bash
git clone https://github.com/ton-utilisateur/mon-projet-git.git
cd mon-projet-git
```

✅ **Résultat attendu**  
Le dépôt est bien cloné localement. Le fichier `README.md` est présent.

👉 **Vérifiez** : via `ls` ou un explorateur de fichiers

---

## 🔹 Partie 2 — Modification du README

1. Ouvrez le fichier `README.md`  
2. Remplacez son contenu par le texte du fichier `TP_Git_Complet.md`  
3. Enregistrez et exécutez :

```bash
git status
git add README.md
git commit -m "Mise à jour du README"
git push origin main
```

✅ **Résultat attendu**  
Le README est mis à jour sur GitHub.

👉 **Vérifiez** : Sur la page d’accueil du dépôt GitHub

---

## 🔹 Partie 3 — Création d’une branche

```bash
git checkout -b develop
```

1. Créez un fichier `notes.md` avec 3 idées de projets ou des notes  
2. Puis :

```bash
git add notes.md
git commit -m "Ajout de notes"
git push origin develop
```

✅ **Résultat attendu**  
Branche `develop` créée avec `notes.md` visible sur GitHub

👉 **Vérifiez** : Via l’onglet "branches" ou "code"

---

## 🔹 Partie 4 — Structure du projet

Dans `develop`, créez cette arborescence :

```
projet/
├── src/
│   └── main.py
├── data/
│   └── sample.txt
└── README.md
```

Dans `main.py` :

```python
print("Hello Git")
```

```bash
git add .
git commit -m "Structure de projet"
git push origin develop
```

✅ **Résultat attendu**  
Structure de dossier bien visible sur GitHub

👉 **Vérifiez** : Explorez la branche `develop`

---

## 🔹 Partie 5 — Merge via Pull Request

1. Allez sur GitHub > **Compare & pull request**  
2. Ajoutez un commentaire, cliquez sur **Create pull request**  
3. Cliquez sur **Merge pull request**  
4. (Optionnel) Supprimez `develop` → **Delete branch**

✅ **Résultat attendu**  
Fusion réussie, branche supprimée ou intégrée à `main`

👉 **Vérifiez** : onglet Pull Requests / historique de commits

---

## 🔹 Partie 6 — Revenir en arrière : `git revert`

```bash
git log --oneline
git revert <commit_id>
```

✅ **Résultat attendu**  
Un nouveau commit annule un précédent

👉 **Vérifiez** : `git log` montre le commit de revert

---

## 🔹 Partie 7 — Réinitialiser l’historique : `git reset`

Sur une branche temporaire :

```bash
git reset --soft HEAD~1   # Conserve les modifs
git reset --mixed HEAD~1  # Supprime du staging
git reset --hard HEAD~1   # ⚠️ Supprime tout
```

✅ **Résultat attendu**  
Compréhension des types de reset

👉 **Vérifiez** : `git log`, `git status`

---

## 🔹 Partie 8 — Gérer un conflit

1. Créez `conflict-a` et `conflict-b`  
2. Modifiez une même ligne dans un fichier  
3. Merge `conflict-a` dans `main`, puis essayez avec `conflict-b`  
4. Résolvez le conflit :

```bash
git add <fichier>
git commit
```

✅ **Résultat attendu**  
Le conflit est résolu proprement

👉 **Vérifiez** : `git log`, contenu du fichier

---

## 🔹 Partie 9 — Copier un commit : `git cherry-pick`

```bash
git log other-branch
git cherry-pick <commit_id>
```

✅ **Résultat attendu**  
Le commit est copié dans `main`

👉 **Vérifiez** : `git log`

---

## 🔹 Partie 10 — Manipulations avec IntelliJ IDEA

### 🔸 Faire un commit

1. Créez `hello.py` :

```python
print("Bonjour depuis IntelliJ !")
```

2. Clic droit → Git → Add  
3. Commit → "Commit and Push"

### 🔸 Travailler avec des branches

- En bas à droite → `main` → **New Branch**
- Travaillez → Commit → retour sur `main` → **Merge Changes**

### 🔸 Push / Pull

- Git → **Push**
- Git → **Pull**

✅ **Résultat attendu**  
Les commits sont visibles dans Git et sur GitHub

👉 **Vérifiez** : Git > Log

---

## 🔹 Partie 11 — Fonctions avancées avec IntelliJ IDEA

### 🔸 Revert

- Git → Log → clic droit → **Revert Commit**

### 🔸 Reset

- Git → Log → clic droit → **Reset Current Branch to Here...**

### 🔸 Résolution de conflits

- Git → **Merge Conflicts**  
- Interface visuelle pour résoudre

### 🔸 Cherry-pick

- Git → Log → clic droit → **Cherry-pick**

✅ **Résultat attendu**  
Toutes les actions peuvent être réalisées via IntelliJ

👉 **Vérifiez** : Git > Log

---

## 🏁 Conclusion

🎉 **Félicitations !** Tu viens de parcourir tout le cycle de travail Git/GitHub  
🧠 Tu maîtrises maintenant **Git en ligne de commande et avec IntelliJ IDEA**
