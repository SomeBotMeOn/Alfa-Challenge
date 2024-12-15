# Alfa-Challenge

## Описание проекта
Проект был разработан в рамках хакатона **Alfa Challenge**. Его цель—предсказать, какие клиенты банка сохранят положительный баланс на своих счетах. Банк заинтересован в минимизации числа клиентов с обнулением баланса, так как это нежелательный исход.

## Метрика качества
Для оценки качества модели в проекте использовалась метрика WMAE (Weighted Mean Absolute Error).

---

## Структура проекта

### Jupyter Notebooks

1. **`Alfa-Create-Data.ipynb`**  
   Подготовка и создание набора данных для обучения моделей:
   - Featuretools
   - RandomForestClassifier

3. **`Alfa-EDA.ipynb`**  
   Исследовательский анализ данных (EDA)

4. **`Alfa-Catboost-Default.ipynb`**  
   Обучение модели CatBoost с параметрами по умолчанию
   - CatBoost
   - **Score**: 0.80881
    
6. **`Alfa-Catboost-Optuna.ipynb`**
   Оптимизация гиперпараметров CatBoost с использованием Optuna
   - Optuna
   - CatBoost

8. **`Alfa-Catboost-With-Best-Params.ipynb`**  
   Итоговое обучение модели CatBoost с оптимальными параметрами
   - CatBoost
   - **Score**: 0.75619 (**лучшая модель**)

10. **`Alfa-LightGBM-Optuna.ipynb`**  
   Оптимизация гиперпараметров LightGBM с помощью Optuna
    - LightGBM

12. **`Alfa-AutoML.ipynb`**  
   Использование библиотеки LightAutoML для автоматического построения модели:
    - LightAutoML
   **Score**: 0.81842

14. **`Alfa-Blending.ipynb`**  
   Объединение предсказаний различных моделей (блендинг):
    - CatBoost
    - LightGBM
    - RandomForestRegressor
    - **Score**: 1.01016

16. **`Alfa-Stacking.ipynb`**  
   Использование стекинга моделей для повышения точности
    - RandomForestRegressor
    - CatBoost
    - LightGBM
    - XGBoost

18. **`Alfa-Check-Score-Of-Models.ipynb`**  
    Сравнение и проверка качества моделей
    - RandomForestRegressor
    - CatBoost
    - LightGBM
    - XGBoost
    - **Score**: 0.87248
---

## Результаты
- **Лучшая модель**: `Alfa-Catboost-With-Best-Params.ipynb` с **Score**: 0.75619

---

## Требования
- Python 3.8+
- Установленные библиотеки:
  - Pandas, Numpy
  - Matplotlib, Seaborn
  - Featuretools, Woodwork
  - CatBoost, LightGBM, XGBoost, LightAutoML
  - Optuna
  - Scikit-learn

---

## Заключение
Этот проект был разработан в рамках хакатона Alfa Challenge

