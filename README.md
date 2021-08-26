# Когортный анализ пользовательской активности сайта Kaggle
## Постановка задачи
### Данные
В проекте были использованы данные пользовательской активности сайта Kaggle, которые показывают, как пользователи создают Kernels (чаще всего Jupyter-ноутбуки), в которых решается та или иная задача, связанная с анализом данных. Данные предоставлены за 18 месяцев, в период с 2019-01-01 по 2020-06-10. 
### Задачи проекта
- Проанализировать активность пользователей и их приток на протяжении всего периода;
- Выделить когорты пользователей по времени присоединения;
- Построить retention curves для раннее выделенных когорт;
- Выделить сегменты внутри когорт на основе используемого языка программирования и проанализировать их активность;
- Построить когортную матрицу retention как для всех пользователей, так и для ее сегментов;
- Сформулировать рекоммендации для улучшения продукта. 
## Результаты
### Выводы
1. Когорта первых двух недель 1го месяца (cohort_size был 14 дней, а две когорты брались с 60 дневной разницей) обладает более высоким retention, чем когорта пользователей первых двух недель 3-го месяца. Следовательно, retention rate новых пользователей падает по сравнению с пользователями, которые присоединились достаточно давно. 
  ** Рекомендация 1:** Возможно, стоит разработать новую стратегию удержания пользователей, обратившись к ранним практикам, например, можно ввести систему лояльности. 
  
2. Сегменты пользователей, использующих языки с ID 8 и 9, ведут себя практически одинаково, это может быть связано с тем, что там учитываются одни и те же пользователи, которые пишут скрипты на 8 и на 9 языке одновременно. Это требует дополнительного исследования. 

3.  Пользователи, использующие остальные языки (не с ID 8 и 9) меньше взаимодействуют с платформой, особенно в начале анализируемого периода. Возможно, это связано с тем, что эти языке менее популярны и поэтому нет надобности в их частом использовании, но также проблема может быть в наличии более популярных и удобных аналогичных сервисов. 
    **Рекомендация 2:** Проанализировать конкурентов, предлагающих аналогичные услуги, и создать стратегию привличения и удержания пользователей третьего сегмента (языки с ID не 8 и не 9)
  
4. У более поздних когорт увеличивается retention на второй месяц. Поэтому можно говорить о некотором улучшении сервиса, а также, возможно, о нацеленности бизнес стратегии на удержание пользователей и эволюцию в этом направлении. Кроме того, видимо, у маркетинговых кампаний, привлекающих пользователей, улучшилось таргетирование, и они стали приводить более целевую аудиторию. 
   **Рекомендация 3:** Продолжать использовать выбранную маркетинговую стратегия, улучшая ее таргетированность. 
  
5. На когортных матрицах retention заметна сильная потеря пользователей на второй месяца использования. 
   ** Рекомендация 4: **Сфокусироваться на удержании пользователей после одного месяца использования продукта и далее.  

