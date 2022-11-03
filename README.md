# MIMIC-IV
Zet de gepreproceste data in een map "/data/". Deze staat ook in de .gitignore, dus hij zal niet meegepusht worden.

## Preprocessing
Nog onder constructie ^_^

Het idee is om uiteindelijk de belangrijke data tabellen per ethniciteit op te slaan als .csv in de map /data/. 

### Preprocessing_I
Deze file selecteert de belangrijke data tabellen en kolommen en merged deze. Voor iedere ethniciteit wordt er een .csv opgeslagen in /data/preprocessing_I/.

### Preprocessing_II
Deze file berekend de meest voorkomende ziekte en voegt hiervoor labels toe aan de datasets.

### Preprocessing_III
Deze is er nog niet, maar we moeten nog verder preprocessen (misschien over/under-samplen, outlier detection, feature selection, etc.). Ik zat te denken dat het voor sommige features nice is om een hot encoding toe te passen (bijv. een kolom 'has_label_is_abnormal' gevuld met 0 of 1).

## Exploration en Random_Forest
Deze twee files heb ik voornamelijk gebruikt voor het maken van de quantitative exercise. Hierin staan wat basic stats en plotjes. De random forest is een super basic scikit learn classifier, die nog geoptimalizeerd moet worden (hyperparameters tunen enzo).