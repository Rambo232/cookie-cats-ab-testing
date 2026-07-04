# Cookie Cats A/B Testing: Beyond the Standard Tutorial

[English version](#english-version) | [Russian version](#russian-version)

---

## English Version <a id="english-version"></a>

A deep-dive analysis of the classic mobile game A/B test dataset (moving an in-game "gate" from level 30 to level 40 in Cookie Cats, featuring 90,189 players). While most public notebooks stop at basic retention comparisons, this project goes deeper to investigate hidden patterns, check for statistical anomalies, and address critical analysis pitfalls.

### Key Discovery
The overall negative effect on 7-day retention (−0.82 p.p.) hides a more nuanced reality:
*   **Casual Players:** Show almost zero change in behavior.
*   **Highly Engaged Players:** Experience a negative impact three times stronger (−2.53 p.p.).

> *Note: This insight is transparently flagged as a post-hoc finding (segments chosen after data exploration) rather than a definitive fact. A dedicated section in the notebook addresses the limitations of this analysis.*

### What Was Done
*   **Data Sanitation:** Screened for missing values, duplicates, and outliers.
*   **Sample Ratio Mismatch (SRM):** Checked the fairness of user assignment across groups.
*   **Power Analysis:** Calculated the Minimum Detectable Effect (MDE) the test could actually capture.
*   **Multiple Testing Correction:** Adjusted hypothesis tests to account for evaluating two metrics simultaneously.
*   **Engagement Metric Audit:** Evaluated total game rounds played.
*   **User Segmentation:** Analyzed results by engagement levels, uncovering the core finding.
*   **Bootstrapping:** Cross-verified parametric test results using non-parametric resampling.
*   **Limitations Review:** Drafted a critical assessment of the experiment's weak spots.

### Summary & Recommendation
**Do not move the gate to level 40 without further validation.**
The data strongly argues against the move, particularly for your most active players. However, because the significance boundaries are narrow and certain questions regarding SRM and post-hoc segmentation remain open, a follow-up experiment is highly recommended.

### Repository Structure
*   `cookie-cats-ab-testing.ipynb` — Full analysis notebook with code, data visualizations, and detailed statistical conclusions.
*   `cookie_cats.csv` — Raw dataset containing 90,189 rows (Source: Open DataCamp / Kaggle dataset "Mobile Games A/B Testing — Cookie Cats").

### Tech Stack
*   **Language:** Python
*   **Data Manipulation:** Pandas, NumPy
*   **Statistical Analysis:** SciPy, Statsmodels (`proportions_ztest`, power analysis)
*   **Visualization:** Matplotlib, Seaborn

### Getting Started

**Install dependencies:**
```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter
```

------------------------------------------------------------------------------------------


# Cookie Cats A/B Testing: Beyond the Standard Tutorial

[English version](#english-version) | [Russian version](#russian-version)

---

## Russian Version <a id="russian-version"></a>

Подробный анализ классического датасета A/B-тестирования в мобильной игре Cookie Cats (исследуется перенос внутриигрового пейволла/«ворот» с 30-го на 40-й уровень, выборка — 90 189 игроков). В то время как большинство стандартных туториалов ограничиваются базовым сравнением удержания (retention), в этом проекте мы копнули глубже: изучили скрытые паттерны, проверили данные на статистические аномалии и разобрали главные подводные камни продуктовой аналитики.

### Ключевое открытие
Общий негативный эффект на 7-дневное удержание (−0,82 п.п.) скрывает важные детали:
*   **Казуальные игроки:** Практически не изменили своего поведения.
*   **Высокововлеченные игроки:** Отреагировали на изменения в три раза хуже (−2,53 п.п.).

> *Примечание: Этот инсайт честно обозначен как гипотеза, сформулированная на основе post-hoc анализа (сегменты выделены уже после изучения данных), а не как железобетонный факт. Ограничениям такого подхода посвящен отдельный раздел в ноутбуке.*

### Что было сделано
*   **Очистка данных:** Проверил датасет на пропуски, дубликаты и аномальные выбросы.
*   **Sample Ratio Mismatch (SRM):** Убедились в корректности сплитования пользователей по группам.
*   **Анализ мощности:** Рассчитали минимально обнаруживаемый эффект (MDE), который тест реально способен зафиксировать.
*   **Поправка на множественное тестирование:** Скорректировали оценку гипотез, так как проверяли две метрики одновременно.
*   **Аудит метрик вовлеченности:** Оценили общее количество сыгранных раундов.
*   **Сегментация аудитории:** Изучили результаты на разных уровнях вовлеченности, что и помогло найти главный инсайт.
*   **Бутстрэпинг:** Перепроверили выводы параметрических тестов с помощью непараметрического ресэмплинга.
*   **Анализ ограничений:** Сформулировали критическую оценку слабых мест проведенного эксперимента.

### Итоги и рекомендации
**Не стоит переносить «ворота» на 40-й уровень без дополнительной проверки.**
Данные явно говорят против этого шага, особенно если смотреть на поведение самых активных игроков. Тем не менее, из-за пограничной статистической значимости, а также открытых вопросов к SRM и post-hoc сегментации, мы настоятельно рекомендуем запустить повторный, более чистый эксперимент.

### Структура репозитория
*   `cookie-cats-ab-testing.ipynb` — Полный ноутбук с анализом, кодом, графиками и подробными статистическими выводами.
*   `cookie_cats.csv` — Исходный датасет на 90 189 строк (Источник: курс Open DataCamp / Kaggle-датасет "Mobile Games A/B Testing — Cookie Cats").

### Стек технологий
*   **Язык:** Python
*   **Работа с данными:** Pandas, NumPy
*   **Статистический анализ:** SciPy, Statsmodels (`proportions_ztest`, power analysis)
*   **Визуализация:** Matplotlib, Seaborn

### Начало работы

**Установка зависимостей:**
```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter
```
