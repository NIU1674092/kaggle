# Classificació de Bolets

## Descripció del Projecte
Aquest projecte té com a objectiu desenvolupar i avaluar models de Machine Learning per classificar si un bolet és comestible o verinós. Per aconseguir-ho, hem utilitzat un conjunt de dades que conté 23 atributs categòrics sobre les característiques dels bolets.

S'han provat i optimitzat quatre models de classificació:
1. *Decision Tree*
2. *KNN (k-Nearest Neighbors)*
3. *SVM (Support Vector Machines)*
4. *Regressió Logística*

---

## Dades del Dataset
El dataset conté 8.124 mostres amb els següents atributs:
- **class (target):** e (comestible) o p (verinós).
- Altres 22 atributs categòrics com cap-shape, cap-color, stalk-root, etc.

Els valors faltants (?) a la columna stalk-root han estat imputats utilitzant probabilitats condicionals segons la classe (e o p).

---

## Estructura del Projecte

### 1. Exploració Inicial de les Dades (EDA)
- Anàlisi de distribucions per atributs.
- Identificació de valors faltants i gestió dels ?.
- Visualització de correlacions entre atributs.

### 2. Preprocessament
- Codificació de variables categòriques utilitzant OrdinalEncoder.
- Divisió del conjunt de dades en entrenament i test (70%/30%).
- Imputació dels valors faltants en stalk-root segons la classe.

### 3. Modelat
S'han provat quatre models amb els hiperparàmetres inicials:
- *Decision Tree*
- *KNN*
- *SVM*
- *Regressió Logística*

Després, s'han ajustat els hiperparàmetres utilitzant *GridSearchCV* per optimitzar el rendiment de cada model.

### 4. Avaluació
- S'han calculat mètriques com *Recall, **Accuracy*, i s'han generat matrius de confusió.
- També s'ha visualitzat la corba PR (Precision-Recall) per a cada model.

---

Per executar l'informe fer: jupyter notebook mushrooms_classification.ipynb