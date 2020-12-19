## Линейни структури:
**1.** Динамичен масив (вектор)  
**2.** Едносвързан списък  
**3.** Двусвързан списък  

## Йерархични структури:  
**1.** Двоично наредено дърво за търсене (Binary search tree)  

## Реализация на *абстрактни* структури от данни:  

**1.Стек**- Добавяне и премахване на елемент от една и съща страна.   
*1 вариант: pushBack && popBack*  
```diff
 |                    | pushBack | popBack |
 |--------------------|----------|---------|
+| Вектор             |   O(1)   |   O(1)  |
-| Едносвързан списък |   O(1)   |   O(n)  |
-| Двусвързан списък  |   O(1)   |   O(1)  |
  ```
  *2 вариант: pushFront && popFront*  
  ```diff
   |                    | pushFront | popFront |
   |--------------------|-----------|----------|
-| Вектор             |   O(n)    |   O(n)   |
+| Едносвързан списък |   O(1)    |   O(1)   |
-| Двусвързан списък  |   O(1)    |   O(1)   |
```
  
**2.Опашка**- Добавяне и премахване на елемент от противоположна страна.  
*1 вариант: pushBack && popFront*  
```diff
 |                    | pushBack | popFront |
 |--------------------|----------|----------|
-| Вектор             |   O(1)   |   O(n)   |
+| Едносвързан списък |   O(1)   |   O(1)   |
-| Двусвързан списък  |   O(1)   |   O(1)   |
  ```
  *2 вариант: pushFront && popBack*  
  ```diff
   |                    | pushFront | popBack |
   |--------------------|-----------|---------|
-| Вектор             |   O(n)    |   O(1)  |
-| Едносвързан списък |   O(1)    |   O(n)  |
-| Двусвързан списък  |   O(1)    |   O(1)  |
```

**3.Приоритетна опашка**.  
* Добавяне с приоритет – добавя елемент на опашката със съответен приоритет.  
* Изваждане на елемента с най-висок приоритет – премахва елемента от опашката, който има най-голям приоритет и го връща.  
Реализация с **двоична пирамида (Binary heap)**.  
[visualisation]( https://visualgo.net/en/heap)
