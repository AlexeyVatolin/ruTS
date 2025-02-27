# Russian Texts Statistics (ruTS)

![ruts](img/ruts.png)

Библиотека для извлечения статистик из текстов на русском языке.

## Функционал

Основной функционал базируется на адаптированных для русского языка статистиках библиотеки [textacy](https://github.com/chartbeat-labs/textacy) и позволяет работать как непосредственно с текстами, так и с подготовленными Doc-объектами библиотеки [spaCy](https://github.com/explosion/spaCy).

Библиотека позволяет:

*   создавать токенизиторы [слов](extractors/words.md) и [предложений](extractors/sentences.md)
*   считать [базовые текстовые статистики](stats/basic_stats.md) (количество слов, предложений, знаков препинания, слогов и др.)
*   считать [метрики удобочитаемости](stats/readability_stats.md) текста (Тест Флеша-Кинкайда, Индекс SMOG, Индекс удобочитаемости LIX и др.)
*   считать [метрики лексического разнообразия](stats/diversity_stats.md) текста (Type-Token Ratio, Measure of Textual Lexical Diversity, Гапакс-индекс и др.)
*   извлекать [морфологические признаки](stats/morph_stats.md) из текста (часть речи, падеж, наклонение, переходность и др.)
*   работать с готовыми текстовыми наборами данных ([Советские христоматии по литературе](datasets/sovchlit.md), [Полное собрание сочинений И.В. Сталина](datasets/stalinworks.md))
*   визуализировать текстовые данные ([Закон Ципфа](visualizers/zipf.md), [Литературная дактилоскопия](visualizers/fingerprinting.md), [Дерево слов](visualizers/word_tree.md))
*   создавать [компоненты](components.md) для встраивания в [spaCy](https://github.com/explosion/spaCy)

## Структура проекта

*   **docs** - документация по проекту
*   **ruts**:
    *   basic_stats.py - базовые текстовые статистики
    *   components.py - компоненты spaCy
    *   constants.py - основные используемые константы
    *   diversity_stats.py - метрики лексического разнообразия текста
    *   extractors.py - инструменты для извлечения объектов из текста
    *   morph_stats.py - морфологические статистики
    *   readability_stats.py - метрики удобочитаемости текста
    *   utils.py - вспомогательные инструменты
    *   **datasets** - наборы данных:
        *   dataset.py - базовый класс для работы с наборами данных
        *   sov_chrest_lit.py - советские хрестоматии по литературе
        *   stalin_works.py - полное собрание сочинений И.В. Сталина
    *   **visualizers** - инструменты для визуализации текстов:
        *   fingerprinting.py - Литературная дактилоскопия
        *   word_tree.py - Дерево слов
        *   zipf.py - Закон Ципфа
*   **tests**:
    *   test_basic_stats.py - тесты базовых текстовых статистик
    *   test_components.py - тесты компонентов spaCy
    *   test_diversity_stats.py - тесты метрик лексического разнообразия текста
    *   test_extractors.py - тесты инструментов для извлечения объектов из текста
    *   test_morph_stats - тесты морфологических статистик
    *   test_readability_stats.py - тесты метрик удобочитаемости текста