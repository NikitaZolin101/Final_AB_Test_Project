FINAL AB TEST PROJECT

Описание датасета
Файл final_results_to_analyze.csv содержит результаты A/B-теста стримингового сервиса.

Поля:
- date
- client_id
- views
- clicks
- start_watch
- finish_watch
- watch_time
- adds_to_fav
- ab_group

Структура проекта

data/
  stream_events.csv
  final_results_to_analyze.csv

notebooks/
  01_EDA.ipynb
  02_Experiment_Design.ipynb
  03_Generate_AB_Test.ipynb
  04_AB_Test_Analysis.ipynb

Используемые библиотеки
pandas, numpy, matplotlib, scipy, statsmodels

Результаты анализа

CTR:
Control = 0.773
Test = 0.385

Average Watch Time:
Control = 4.10
Test = 6.69

CR_fav:
Control = 0.00
Test = 0.00

ARPU (в учебном примере рассчитан по средней длительности просмотра):
Control = 4.10
Test = 6.69

Итог:
Тестовая группа демонстрирует более высокую среднюю длительность просмотра, однако CTR ниже. Окончательное решение принимается по результатам t-test и bootstrap, представленным в ноутбуке.
