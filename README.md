# Cookie Cats A/B Testing: Beyond the Standard Tutorial

[English version](#english-version) | [Russian version](#russian-version)

---

## English Version <a id="english-version"></a>

A deep-dive analysis of the classic mobile game A/B test dataset (moving an in-game "gate" from level 30 to level 40 in Cookie Cats, featuring 90,189 players). While most public notebooks stop at basic retention comparisons, this project goes deeper to investigate hidden patterns, check for statistical anomalies, and address critical analysis pitfalls.

### 🚀 Key Discovery
The overall negative effect on 7-day retention (−0.82 p.p.) hides a more nuanced reality:
*   **Casual Players:** Show almost zero change in behavior.
*   **Highly Engaged Players:** Experience a negative impact three times stronger (−2.53 p.p.).

> *Note: This insight is transparently flagged as a post-hoc finding (segments chosen after data exploration) rather than a definitive fact. A dedicated section in the notebook addresses the limitations of this analysis.*

### 🛠️ What Was Done
*   **Data Sanitation:** Screened for missing values, duplicates, and outliers.
*   **Sample Ratio Mismatch (SRM):** Checked the fairness of user assignment across groups.
*   **Power Analysis:** Calculated the Minimum Detectable Effect (MDE) the test could actually capture.
*   **Multiple Testing Correction:** Adjusted hypothesis tests to account for evaluating two metrics simultaneously.
*   **Engagement Metric Audit:** Evaluated total game rounds played.
*   **User Segmentation:** Analyzed results by engagement levels, uncovering the core finding.
*   **Bootstrapping:** Cross-verified parametric test results using non-parametric resampling.
*   **Limitations Review:** Drafted a critical assessment of the experiment's weak spots.

### 📊 Summary & Recommendation
**Do not move the gate to level 40 without further validation.**
The data strongly argues against the move, particularly for your most active players. However, because the significance boundaries are narrow and certain questions regarding SRM and post-hoc segmentation remain open, a follow-up experiment is highly recommended.

### 📁 Repository Structure
*   `cookie-cats-ab-testing.ipynb` — Full analysis notebook with code, data visualizations, and detailed statistical conclusions.
*   `cookie_cats.csv` — Raw dataset containing 90,189 rows (Source: Open DataCamp / Kaggle dataset "Mobile Games A/B Testing — Cookie Cats").

### 💻 Tech Stack
*   **Language:** Python
*   **Data Manipulation:** Pandas, NumPy
*   **Statistical Analysis:** SciPy, Statsmodels (`proportions_ztest`, power analysis)
*   **Visualization:** Matplotlib, Seaborn

### ⚙️ Getting Started

**Install dependencies:**
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter


------------------------------------------------------------------------------------------


# Cookie Cats A/B Testing: Beyond the Standard Tutorial

[English version](#english-version) | [Russian version](#russian-version)

---

## Russian Version <a id="russian-version"></a>

Глубокий анализ классического датасета A/B-тестирования в мобильной игре (перенос внутриигровых «ворот» с 30-го на 40-й уровень в Cookie Cats с участием 90 189 игроков). В то время как большинство публичных блокнотов ограничиваются базовым сравнением удержания (retention), этот проект идет дальше, чтобы исследовать скрытые закономерности, проверить статистические аномалии и разобрать критические ловушки анализа.

### 🚀 Ключевое открытие
Общий негативный эффект на 7-дневное удержание (−0,82 п.п.) скрывает более нюансированную картину:
*   **Казуальные игроки:** Практически не меняют своего поведения.
*   **Высокововлеченные игроки:** Демонстрируют в три раза более сильный негативный эффект (−2,53 п.п.).

> *Примечание: Этот инсайт открыто обозначен как post-hoc находка (сегменты выбраны после изучения данных), а не как окончательный факт. Ограничениям такого анализа посвящен отдельный раздел в блокноте.*

### 🛠️ Что было сделано
*   **Очистка данных:** Проверка на пропущенные значения, дубликаты и выбросы.
*   **Sample Ratio Mismatch (SRM):** Проверка корректности и честности распределения пользователей по группам.
*   **Анализ мощности:** Расчет минимально обнаруживаемого эффекта (MDE), который тест реально мог зафиксировать.
*   **Поправка на множественное тестирование:** Корректировка гипотез с учетом одновременной оценки двух метрик.
*   **Аудит метрик вовлеченности:** Оценка общего количества сыгранных игровых раундов.
*   **Сегментация пользователей:** Анализ результатов по уровням вовлеченности, который и выявил ключевой инсайт.
*   **Бутстрэпинг:** Перекрестная проверка результатов параметрических тестов с помощью непараметрического ресэмплинга.
*   **Обзор ограничений:** Подготовка критической оценки слабых мест эксперимента.

### 📊 Итоги и рекомендации
**Не переносите ворота на 40-й уровень без дополнительной валидации.**
Данные решительно выступают против этого переноса, особенно в отношении ваших самых активных игроков. Однако из-за узких границ значимости, а также открытых вопросов касательно SRM и post-hoc сегментации, настоятельно рекомендуется провести повторный эксперимент.

### 📁 Структура репозитория
*   `cookie-cats-ab-testing.ipynb` — Полный блокнот с анализом, кодом, визуализациями данных и подробными статистическими выводами.
*   `cookie_cats.csv` — Исходный датасет, содержащий 90 189 строк (Источник: датасет Open DataCamp / Kaggle "Mobile Games A/B Testing — Cookie Cats").

### 💻 Стек технологий
*   **Язык:** Python
*   **Работа с данными:** Pandas, NumPy
*   **Статистический анализ:** SciPy, Statsmodels (`proportions_ztest`, анализ мощности)
*   **Визуализация:** Matplotlib, Seaborn

### ⚙️ Начало работы

**Установка зависимостей:**
```bash
pip install pandas numpy scipy statsmodels matplotlib seaborn jupyter
```

