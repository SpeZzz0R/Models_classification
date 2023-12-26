# Models_classification
https://colab.research.google.com/drive/13WEJuSOLlz08uRg_ObKPsA2R4htxAiqk
https://nbviewer.org/github/SpeZzz0R/Models_classification/blob/main/models_classification.ipynb

## О проекте
Анализ данных с помощью различных моделей машинного обучения.  
Тип задачи - классификация (два класса - 0 и 1).  
Цель - определение модели, показывающей самую высокую точность предсказания.  
Исходные данные сгенерированы с помощью функции "make_classification". Разделение классов - нечеткое, чтобы продемонстрировать преимущества "сложных" моделей прогнозирования с большим количеством настраиваемых параметров.    


## Используемые технологии
- Google Colab / Jupyter Notebook
- Python
- Pandas
- Numpy
- Matplotlib
- Scikit-learn  


## Таблица метрических показателей моделей
|         Model         | Log Loss |  Score   |   AUC   |     F1      |  Precision  |   Recall    | Accuracy |   TN, FP, FN, TP    | 
|:---------------------:|:--------:|:--------:|:-------:|:-----------:|:-----------:|:-----------:|:--------:|:--------------------:|
|  Logistic Regression  |  0.4574  |  0.7867  |  0.844  | 0.84 / 0.67 | 0.81 / 0.74 | 0.88 / 0.61 |   0.79   | 2294, 305, 548, 853  |
|          MLP          |  0.1482  |  0.9413  |  0.984  | 0.96 / 0.91 | 0.94 / 0.95 | 0.97 / 0.88 |   0.94   | 2527, 72, 163, 1238  |
|       CatBoost        |  0.1639  |  0.9383  |  0.981  | 0.95 / 0.91 | 0.93 / 0.95 | 0.97 / 0.87 |   0.94   | 2528, 71, 176, 1225  |
|    Random Forest      |  0.1998  |  0.9293  |  0.977  | 0.95 / 0.89 | 0.92 / 0.94 | 0.97 / 0.85 |   0.93   | 2523, 76, 207, 1194  |
|          KNN          |  0.3239  |  0.9105  |  0.965  | 0.93 / 0.86 | 0.90 / 0.94 | 0.97 / 0.80 |   0.91   | 2522, 77, 281, 1120  |
|          SVM          |  0.1757  |  0.9323  |  0.980  | 0.95 / 0.90 | 0.93 / 0.95 | 0.97 / 0.86 |   0.93   | 2530, 69, 202, 1199  |
|     Naive Bayes       |  0.5417  |  0.7688  |  0.851  | 0.81 / 0.70 | 0.86 / 0.64 | 0.78 / 0.76 |   0.77   | 2015, 584, 341, 1060 |

Параметры F1, Precision, Recall представлены в следующем формате: значение для класса 0 / значение для класса 1.  


## Выбор модели

Самые точные результаты выдает модель MLP, далее CatBoost, ненамного отстает SVM. Здесь все довольно предсказуемо. Выигрывают те модели, которые позволяют делать настройку с помощью большого количества параметров. И самые лучшие результаты показывает Многослойный перцептрон (MLP), основанный на нейронных сетях, что довольно предсказуемо. НО!, чтобы добиться высокой точности результатов, необходимо подбирать значения параметров. Большую помощь в этом оказывает случайный (рандомизированный) поиск - RandomizedSearchCV().

Самая неточная модель - Naive Bayes, чуть поточнее Logistic Regression. Что немного удивительно. В большинстве случаев, самые грубые результаты показывают линейные модели (в данной задаче Logistic Regression). Скорее всего, Наивный Байес совершенно не подходит для данной задачи или параметры выбраны неверно.   


==============================

> Автором проекта является Middle Data Scientist
> 
> Запесочный Владислав.
> 
> Страница на github: https://github.com/SpeZzz0R  
> 

