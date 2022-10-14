# MIMIC-IV
## Preprocessing
Nog onder constructie ^_^

Het idee is om uiteindelijk de belangrijke data tabellen per ethniciteit op te slaan als .csv. 

### Preprocessing_I
Deze file selecteert de belangrijke data tabellen en kolommen en merged deze. Voor iedere ethniciteit wordt er een .csv opgeslagen in /data/preprocessing_I/. Vanaf daar moeten we nog verder preprocessen (misschien over/under-samplen, outlier detection, feature selection, etc.). Ik zat te denken dat het voor sommige features nice is om een hot encoding toe te passen (bijv. een kolom 'has_label_is_abnormal' gevuld met 0 of 1).