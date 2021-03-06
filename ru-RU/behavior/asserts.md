---
name: Проверки
---

# Проверка состояния (Assertions)

```
TODO расширить описание примерами из step definition

```

@простые проверки

	ПередатьНаПроверку(чтоТо1, ДолжноРавняться, чтоТо2)
	ПередатьНаПроверку(чтоТо1, НеДолжноРавняться, чтоТо2)
	ПередатьНаПроверку(чтоТо1, ДолжноБытьПодобным, чтоТо2)		
	ПередатьНаПроверку(чтоТо1, НеДолжноБытьПодобным, чтоТо2)
	ПередатьНаПроверку(чтоТо1, ДолжноУказыватьНа, чтоТо2)
	ПередатьНаПроверку(чтоТо1, НеДолжноУказыватьНа, чтоТо2)
	ПередатьНаПроверку(чтоТо1, ДолжноБытьНеопределено)
	ПередатьНаПроверку(чтоТо1, НеДолжноБытьНеопределено)
	ПередатьНаПроверку(чтоТо1, ДолжноБытьИстинной)
	ПередатьНаПроверку(чтоТо1, ДолжноБытьЛожью)
	ПередатьНаПроверку(чтоТо1, ДолжноБытьНулевымЗначением)

@проверка числовых значений

	ПередатьНаПроверку(1, ДолжноБытьБольше, 0)
	ПередатьНаПроверку(1, ДолжноБытьБольшеИлиРавно, 0)
	ПередатьНаПроверку(1, ДолжноБытьМеньше, 2)
	ПередатьНаПроверку(1, ДолжноБытьМеньшеИлиРавно, 2)
	ПередатьНаПроверку(1.1, ДолжноБытьМежду, .8, 1.2)
	ПередатьНаПроверку(1.1, НеДолжноБытьМежду, 2, 3)
	ПередатьНаПроверку(1.1, ДолжноБытьМеждуИлиРавное, .9, 1.1)
	ПередатьНаПроверку(1.1, НеДолжноБытьМеждуИлиРавно, 1000, 2000)
	ПередатьНаПроверку(1.0, ДолжноПриблизительноРавняться, 0.99999999, .0001)   
	ПередатьНаПроверку(1.0, НеДолжноПриблизительноРавняться, 0.9, .0001)

@проверка коллекций

	ПередатьНаПроверку(универсальнаяКоллекция, ДолжнаСодержать, 4)
	ПередатьНаПроверку(универсальнаяКоллекция, НеДолжнаСодержать, 5)
	ПередатьНаПроверку(4, ДолжноБытьВ, универсальнаяКоллекция)
	ПередатьНаПроверку(4, НеДолжноБытьВ, универсальнаяКоллекция)
	ПередатьНаПроверку(универсальнаяКоллекция, ДолжнаБытьПустой)
	ПередатьНаПроверку(универсальнаяКоллекция, НеДолжнаБытьПустой)
	ПередатьНаПроверку(универсальнаяСтруктура, ДолжнаСодержатьКлюч, "a")
	ПередатьНаПроверку(универсальнаяСтруктура, НеДолжнаСодержатьКлюч, "b")
	ПередатьНаПроверку(универсальнаяКоллекция, ДолжнаИметьДлину , 1) 

@проверка строк

	ПередатьНаПроверку("asdf", ДолжнаНачинатьсяС, "as")
	ПередатьНаПроверку("asdf", НеДолжнаначинатьсяС, "df")
	ПередатьНаПроверку("asdf", ДолжнаЗаканчиваться, "df")
	ПередатьНаПроверку("asdf", НеДолжноЗаканчиваться, "df")
	ПередатьНаПроверку("asdf", ДолжноСодержатьПодстроку, "sd")
	ПередатьНаПроверку("asdf", НеДолжноСодержатьПодстроку, "er")
	ПередатьНаПроверку("adsf", ДолжнаБытьПустой)
	ПередатьНаПроверку("asdf", НеДолжнаБытьПустой)

@проверка исключительных ситуаций
        
	ПередатьНаПроверку("StepName", ДолженВызватьИсключение)
	ПередатьНаПроверку("StepName", НеДолженВызватьИсключение)
	ПередатьНаПроверку("StepName", ДолженВызватьисключениеСТекстом, "Паника ;-)")
	ПередатьНаПроверку("StepName", НеДолженВызватьИсключениеСТекстом, "Cтранное ;-)")	

@проверка типов

	ПередатьНаПроверку(1, ДолжноСовпадатьПоТипуС, 0)
	ПередатьНаПроверку(1, НеДолжноСовпадатьПоТипуС, "asdf")

@проверка временных отрезков

	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиРаньшеЧем, отсечкаВремени2)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиРаньшеИлиВМомент, отсечкаВремени2)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиПозжеЧем, отсечкаВремени2)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиПозжеЧемИлиВМомент, отсечкаВремени2)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиМежду, отсечкаВремени2, отсечкаВремени3)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиМеждуИлиВМомент, отсечкаВремени2, отсечкаВремени3)
	ПередатьНаПроверку(отсечкаВремени1, НеДолжноПроизойтиМеждуИлиВМомент, отсечкаВремени2, отсечкаВремени3)
	ПередатьНаПроверку(отсечкаВремени1, ДолжноПроизойтиВТечении, Длительность, началоОтсчета)
	ПередатьНаПроверку(отсечкаВремени1, НеДолжноПроизойтиВТечении, Длительность, началоОтсчета)

@проверка функций и объектов

	ПередатьНаПроверку(_объект, ДолженИметьСвойство, имяСвойсвта)
	ПередатьНаПроверку(_объект, ДолженИметьПроцедуру, имяМетода)
	ПередатьНаПроверку(_объект, ДолженИметьФункцию, имяМетода)
	ПередатьНаПроверку(ДолжнаБытьГлобальнаяПроцедура, имяМетода)
	ПередатьНаПроверку(ДолжнаБытьГлобальнаяФункция, имяМетода)

@проверка служебных типов 1С



#todo расширить объектами 1С






