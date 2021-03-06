#term4 au project

###Список задач (initial):

* ~~Нахождение и выделение нецензурной лексики, наиболее быстрый алгоритм~~
* ~~Тесты~~
* ~~Профиллирование работы~~
* ~~Приведение кода в лицеприятное состояние~~
* JavaScript

###Информация о выборке
![Граффик](src/test/resources/plots/length_number_plot.png "Граффик") <br />
Реальный пример текста:
```
всем пака с вами был данил 92 жди 12 части
рости шамбарова да жалуйся в групе я тебя не баюсь да пашол ты в ростик шамбарова
я тебя не баюсь я не буду руский учит зазазазазазазазаз
ростик шамбарова меня не жэляют это тебя жэлеют тваи видео
дажэ я тебя пажэлел ты лох и не саревнуйся са мной у меня большэ лайков
```

###Результаты
![Граффик](src/test/resources/plots/length_time_plot.png "Граффик") <br />
Всего слов:  1196 <br />
Забанено слов:  56 <br />
Считали edit1_dist для слов:
```
 ['ёбаный', 'срана', 'сраной', 'ебаном', 'ебан', 'хх', 'искуссный', 'искуссно', 'озерцы', 'озерцы', 'озерцов', 'че', 'рмазь', 'прасто', 'писдец', 'работк', 'утести', 'убевать', 'сколко', 'сколкий', 'скольк', 'ёвр', 'евр', 'евра', 'ща', 'ёвр', 'евр', 'евра', 'сломон', 'сломона', 'ангелишка', 'ангелишка', 'молоци', 'молодци', 'короч', 'прекола', 'прекол', 'ипать', 'познакомтесь', 'диппер', 'всвязь', 'чё', 'неть', 'паучочек', 'россомаха', 'апакалипсис', 'апакалипсис', 'ево', 'сабак', 'сабака', 'аааа', 'сыкло', 'званить', 'доктара', 'штоп', 'щя', 'вылечело', 'рость', 'шамбаров', 'група', 'груп', 'шамбаров', 'руский', 'шамбаров', 'твай', 'гавный', 'гавно', 'дажэ', 'саревноваться', 'са', 'большэ', 'файта', 'пабедил', 'пабедить', 'прохажа', 'прохаж', 'дриться']
```
Считали edit2_dist для слов:
```
 ['сраныть', 'ебанома', 'ебашим', 'ебашить', 'озерцовский', 'нибыть', 'нибудь', 'озерцовый', 'ахуесть', 'ебануться', 'ебожить', 'тебянужный', 'ангелишек', 'ангелишек', 'мейбл', 'грэвитя', 'странногедон', 'диппереть', 'дипперо', 'мейбл', 'стемфорд', 'стемфорда', 'avengеrs', 'фьюри', 'дедпул', 'дедпулом', 'паучочека', 'фьюри', 'нибыть', 'нибудь', 'охренела', 'начосс', 'наканецтый', 'лесницэ', 'геганский', 'геганскай', 'атамстить', 'астолавист', 'астолавистый', 'выылечело', 'выылечесть', 'вылечесть', 'пашол', 'жэлять', 'жэлеть', 'пажэлела', 'пажэлеть', 'хыдыщь', 'хыдыщить', 'крипипаста', 'выжэвалка', 'выжэвалок', 'слэндёр', 'слэндёр', 'такштый']
```
Долго обрабатывали слова (выше "fast" линии):
```
 ['ебашим', 'озерцовские', 'странногедон', 'стемфорд', 'дедпулом', 'наканецто', 'геганская', 'астолависта', 'выылечел', 'вылечел', 'пажэлел', 'выжэвалку']
```


***

Текущая скорость распознавания: **~6100-8000** слов в секунду на реальных данных (хорошо?) <br />
Текущая точность распознавания: **100%** (плохие тесты, мало матов, много ошибок)

###Как улучшить?
* ~~Использовать другую структуру данных, есть DatTrie и CharTrie, HatTrie уже пробовал: медленнее. Общая ситуация такая: быстрее стандартного dict вроде нет, но память можно улучшить, пожертвовав скоростью. (память)~~
* ~~Две вставки это много? Да вроде, нет. (скорость)~~
* Частота употребления: можно дать матам частоту и скачать словарь частотности обычных слов. (точность)
* ~~Mystem? Слишком долго.~~
* ~~Запоминать уже посмотренные слова? Ленивая обработка. (скорость)~~
* ~~Предпосчитать самые популярные обынчые слова (первые 20-30k (~150mb) из словаря частотности), поэтому считать edit_dist2 мы будем только для самых редких слов с как минимум 2 ошибками, к тому же их вообще мало. (точность & скорость)~~
* ~~Два слова подряд без пробела. (точность, после вероятностей)~~
* Анализировать по 2-3 слова, списки можно взять у opencorpora. (точность)
* Добавить современных слов и имен собственных. (часть Виталика, точность и скорость)

###Задачи (22.05.16)
* ввести вероятности + максимально улучшить код
* code style to more object-orient
* node.js
* code review
* написать в readme подробней про алгоритм
* скрыть коммиты матных словарей
* ~~многопоточность (1 поток = 1 слово)~~ [result: долго, нужно другое дробление]





