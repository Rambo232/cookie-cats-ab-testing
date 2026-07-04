Cookie Cats A/B Testing: Beyond the Standard TutorialA deep-dive analysis of the classic mobile game A/B test dataset (moving an in-game "gate" from level 30 to level 40 in Cookie Cats, featuring 90,189 players). While most public notebooks stop at basic retention comparisons, this project goes deeper to investigate hidden patterns, check for statistical anomalies, and address critical analysis pitfalls.🚀 Key DiscoveryThe overall negative effect on 7-day retention (−0.82 p.p.) hides a more nuanced reality:Casual Players: Show almost zero change in behavior.Highly Engaged Players: Experience a negative impact three times stronger (−2.53 p.p.).Note: This insight is transparently flagged as a post-hoc finding (segments chosen after data exploration) rather than a definitive fact. A dedicated section in the notebook addresses the limitations of this analysis.🛠️ What Was DoneData Sanitation: Screened for missing values, duplicates, and outliers.Sample Ratio Mismatch (SRM): Checked the fairness of user assignment across groups.Power Analysis: Calculated the Minimum Detectable Effect (MDE) the test could actually capture.Multiple Testing Correction: Adjusted hypothesis tests to account for evaluating two metrics simultaneously.Engagement Metric Audit: Evaluated total game rounds played.User Segmentation: Analyzed results by engagement levels, uncovering the core finding.Bootstrapping: Cross-verified parametric test results using non-parametric resampling.Limitations Review: Drafted a critical assessment of the experiment's weak spots.📊 Summary & RecommendationDo not move the gate to level 40 without further validation.The data strongly argues against the move, particularly for your most active players. However, because the significance boundaries are narrow and certain questions regarding SRM and post-hoc segmentation remain open, a follow-up experiment is highly recommended.📁 Repository Structurecookie-cats-ab-testing.ipynb — Full analysis notebook with code, data visualizations, and detailed statistical conclusions.cookie_cats.csv — Raw dataset containing 90,189 rows (Source: Open DataCamp / Kaggle dataset "Mobile Games A/B Testing — Cookie Cats").💻 Tech StackLanguage: PythonData Manipulation: Pandas, NumPyStatistical Analysis: SciPy, Statsmodels (proportions_ztest, power analysis)Visualization: Matplotlib, Seaborn⚙️ Getting StartedInstall dependencies:bashpip install pandas numpy scipy statsmodels matplotlib seaborn jupyter
Use code with caution.Launch the notebook:bashjupyter notebook cookie-cats-ab-testing.ipynb
Use code with caution.



Cookie Cats A/B Test — разбор глубже стандартного туториала
Разбор известного учебного датасета A/B-теста (перенос игрового «шлюза» с уровня 30 на уровень 40 в мобильной игре Cookie Cats, 90 189 игроков). Большинство публичных решений этого датасета сравнивают retention между группами и на этом останавливаются. Здесь — попытка пойти дальше и специально проверить то, что обычно пропускают, заодно закрывая для себя пробел по статистике и A/B-тестированию.
Главная находка
Средний эффект на retention_7 (−0.82 п.п.) скрывает то, что при разбивке игроков по вовлечённости эффекта почти нет у случайных игроков, но он втрое сильнее у самых активных (−2.53 п.п.). Помечено честно как находка постфактум (сегменты выбраны уже после того, как увидел данные), а не как железно доказанный факт — в ноутбуке есть отдельный раздел с разбором слабых мест анализа.
Что сделано
Проверка данных на пропуски, дубликаты, выбросы
Проверка честности разделения на группы (SRM)
Расчёт минимального эффекта, который тест вообще способен заметить (MDE)
Тесты гипотез с поправкой на то, что метрик две
Проверка метрики вовлечённости
Разбивка по сегментам вовлечённости — где нашлась основная находка
Bootstrap как проверка результата другим методом
Отдельный раздел с честным разбором слабых мест анализа
Вывод
Не переносить шлюз на уровень 40 без дополнительной проверки — результат говорит против переноса, особенно для вовлечённых игроков, но граница значимости узкая, а часть вопросов (SRM, сегментация) до конца не закрыта одним прогоном теста.
Файлы
cookie-cats-ab-testing.ipynb — полный разбор с кодом, графиками и выводами
cookie_cats.csv — исходные данные (90 189 строк; источник — открытый датасет DataCamp/ Kaggle "Mobile Games A/B Testing — Cookie Cats")
Стек
Python, Pandas, NumPy, SciPy, statsmodels (proportions z-test, power analysis), Matplotlib, Seaborn
Как запустить
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter

jupyter notebook cookie-cats-ab-testing.ipynb


