---
name: Язык описания требований
---

# Ключевые слова языка GHerkin

* используется при написании исходного кода ожидания от системы
* хранится в файлах с раширением .feature в каталоге features

## Системные значения


```
# encoding: utf-8
# language: ru
```

означают что:

* файл feature имеет кодировку UTF-8 
* использует набор ключевых слов для русской грамматики

Возможные значения

* encoding - констата и всегда равна **utf-8**
* language
 * ru - русские ключевые слова
 * ua - украинские ключевые слова 


## Функционал

отражает проверяемую функциональность и содержит ответ на 3 вопроса

* какую функцию системы хотим проверить
* для какой роли использования
* цель данного функционала


```Gherkin
Функционал: Проверка значений и поведения внутри кода сценариев
	Как Разработчик 
	Я Хочу чтобы в сценариях была возможность проверить значения на ожидаемое состояние


```

## Контекст сценариев


```
TODO
```

## Сценарий 


```
TODO
```

### секция Когда

```
TODO
```

### секция Тогда


```
TODO
```

## Примеры

## Тэги со знаком "@"

используются для дополнительной структуруризации, поиска и фильтрации

например:


```Gherkin

# encoding: utf-8
# language: ru

@IgnoreOnCIMainBuild
@Draft


```



