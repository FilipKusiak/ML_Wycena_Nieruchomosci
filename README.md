# 🚀 Data Science & Machine Learning Portfolio

Cześć! To repozytorium zawiera moje projekty z zakresu uczenia maszynowego (Machine Learning) i analizy danych. Portfolio udowadnia moje zrozumienie pełnego przekroju podstawowych algorytmów ML: od przewidywania wartości ciągłych, przez klasyfikację, aż po uczenie nienadzorowane.

## 📂 Spis projektów

### [1. Kalkulator Wyceny Nieruchomości (Regresja)](./01_Wycena_Nieruchomosci)
* **Technologia:** Python, Pandas, Scikit-Learn (`LinearRegression`)
* **Opis:** Model przewidujący wartość mieszkań na podstawie metrażu, wieku budynku i odległości od centrum. Projekt demonstruje rozumienie korelacji danych i obsługi szumu rynkowego.

### [2. Przewidywanie Odejść Klientów / Churn (Klasyfikacja)](./02_Customer_Churn)
* **Technologia:** Python, Scikit-Learn (`LogisticRegression`, `RandomForestClassifier`), Seaborn
* **Opis:** Model klasyfikacji binarnej wyłapujący klientów zagrożonych rezygnacją z subskrypcji. Projekt zawiera analizę Macierzy Pomyłek (Confusion Matrix) oraz ważności cech (Feature Importance), udowadniając, że czasem prostszy model sprawdza się lepiej.

### [3. Segmentacja Klientów E-commerce (Grupowanie)](./03_Segmentacja_Klientow)
* **Technologia:** Python, Scikit-Learn (`KMeans`), Matplotlib
* **Opis:** Zastosowanie uczenia nienadzorowanego do automatycznego podziału klientów na 4 grupy docelowe (VIP, Oszczędni, itp.) na podstawie ich dochodów i wydatków. Algorytm samodzielnie zidentyfikował klastry bez podawania mu etykiet docelowych.

---
*Projekty zostały stworzone w środowiskach wirtualnych (venv) przy użyciu Jupyter Notebook.*

# 🏠 Kalkulator Wyceny Nieruchomości (Machine Learning)

To jest mój pierwszy projekt w ramach Machine Learningu. Zbudowałem model sztucznej inteligencji, który wycenia wartość mieszkań na podstawie ich parametrów (metraż, liczba pokoi, wiek budynku i odległość od centrum).

## 🚀 Technologie
* **Język:** Python 3.11
* **Biblioteki:** `pandas`, `scikit-learn`, `matplotlib`, `seaborn`
* **Narzędzia:** Jupyter Notebook, środowisko wirtualne `venv`, VS Code

## 🧠 Jak to działa?
1. **Generowanie danych (EDA):** Projekt rozpoczyna się od wygenerowania sztucznego zbioru danych 500 mieszkań z logicznymi zależnościami rynkowymi i dodanym szumem. Na tym etapie generowana jest też mapa korelacji (Heatmap).
2. **Budowa modelu:** Projekt wykorzystuje algorytm **Regresji Liniowej** (`LinearRegression` z pakietu scikit-learn).
3. **Wyniki:** Model z sukcesem odtworzył ukryte wzory wyceny bez znajomości początkowego algorytmu. Średni błąd wyceny (MAE) wynosi ~42 000 zł (jest to wyłącznie błąd wynikający z niemożliwego do przewidzenia, losowego szumu na rynku).

## 🛠️ Jak uruchomić projekt u siebie?

1. Sklonuj to repozytorium na swój komputer:
   ```bash
   git clone [https://github.com/FilipKusiak/ML_Wycena_Nieruchomosci.git](https://github.com/FilipKusiak/ML_Wycena_Nieruchomosci.git)



   ---

## 📉 Projekt 2: Przewidywanie odejść klientów (Customer Churn)

Drugi projekt to **klasyfikacja binarna**. Celem było przewidzenie, czy klient zrezygnuje z subskrypcji na podstawie jego zachowań, wieku i rachunków.

### 🧠 Wykorzystane Algorytmy i Wyniki:
* **Logistic Regression:** Uzyskał wyższą dokładność (**82%**), idealnie dopasowując się do prostych zależności w danych.
* **Random Forest:** Pozwolił na analizę ważności cech (76% accuracy).

### 📊 Co najbardziej wpływa na odejście (Feature Importance):
Dzięki "Lasowi Losowemu" wiemy, co boli klientów:
1. **Miesięczny rachunek:** Najsilniejszy czynnik (pieniądze!).
2. **Staż klienta:** Lojalność rośnie z czasem spędzonym w usłudze.
3. **Liczba telefonów do wsparcia:** Problemy techniczne wypychają ludzi z firmy.

### 💡 Czego się nauczyłem?
Ten projekt pokazał mi, że **większy model nie zawsze jest lepszy**. Random Forest zaczął "kombinować" (overfitting), podczas gdy zwykła Regresja Logistyczna trafiła w punkt.