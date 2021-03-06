# Swift

1. :heavy_check_mark: 1-12 [100 Days of Swift](https://www.hackingwithswift.com/100) :
    1. :heavy_check_mark: [Why can’t Swift add a Double to an Int?](https://www.hackingwithswift.com/quick-start/understanding-swift/why-cant-swift-add-a-double-to-an-int)
    2. :heavy_check_mark: [When should you use a while loop instead of for?](https://www.hackingwithswift.com/quick-start/understanding-swift/when-should-you-use-a-while-loop)
    3. :heavy_check_mark: [When should you use a repeat loop?](https://www.hackingwithswift.com/quick-start/understanding-swift/when-should-you-use-a-repeat-loop)
    4. :heavy_check_mark: [Exiting multiple loops](https://www.hackingwithswift.com/sixty/4/5/exiting-multiple-loops)
    5. :heavy_check_mark: [Why does Swift have labeled statements?](https://www.hackingwithswift.com/quick-start/understanding-swift/why-does-swift-have-labeled-statements)
    6. :heavy_check_mark: [Skipping items](https://www.hackingwithswift.com/sixty/4/6/skipping-items)
    7. :heavy_check_mark: [Variadic functions](https://www.hackingwithswift.com/sixty/5/7/variadic-functions)
    8. :heavy_check_mark: [When to use variadic functions](https://www.hackingwithswift.com/quick-start/understanding-swift/when-to-use-variadic-functions)
   
   
   
## Коллекции (набор значений)

* array (массив) - сохраняют свой порядок и могут содержать дубликаты

<details><summary>Open</summary>
<p>
 
     * Вы можете свободно добавлять к ним данные (если не let), чтобы со временем наращивать свои данные, или вы можете удалить или даже изменить порядок элементов, если хотите.

    * Мы считываем значения из массивов, используя их числовую позицию, отсчитывая от 0. Этот «отсчет от 0» имеет технический термин: zero-based `array.[0]`
  
  > Для сравнения, массивы должны хранить свои элементы в том порядке, в котором вы им указываете, поэтому, 
  > чтобы проверить, существует ли элемент X в массиве, содержащем 10 000 элементов, 
  > Swift необходимо начать с первого элемента и проверять каждый элемент, пока он не будет найден
  
    `var website = ["Apple", "www.apple.com"]`
  
    Получить значения: `website[0]` и `website[1]`
  
</p>
</details>

* tuples (кортеж) - позволяют хранить несколько типов вместе в одном значении; Кортеж - это не коллекции, такие как `Array` или `Dictionary`, а структурированные типы, похожие на структуру без имени


<details><summary>Open</summary>
<p>
 
    * Нельзя добавлять или удалять элементы из кортежа: кортежи фиксированы по размеру.
    
    * Нельзя изменить тип элементов в кортеже; они всегда имеют те же типы, с которыми были созданы.
    
    * Нельзя получить доступ к элементам в кортеже, используя числовые позиции или называя их, но Swift не позволит вам читать числа или имена, которых не существует.

    `struct Person {
      let name: String
      let age: Int
      let isMarried: Bool
    }`
  
    `var person: Person = Person(name: "Paul", age: 40, isMarried: true)`
  
    `var person = (name: "Paul", age: 40, isMarried: true)`
  
    Получить значения: `person.name`, `person.age`, `person.0`
   
    почти то же самое что и
  
    `struct Person {
      let name: String
      let age: Int
      let isMarried: Bool
    }`
  
    `var person: Person = Person(name: "Paul", age: 40, isMarried: true)`
  

    >  Кортежи дают нам некоторую безопасность имен кортежей, но могут расти и изменяться, как массивы
  
</p>
</details>

* set (множество) - неупорядочены и не могут содержать дубликатов


<details><summary>Open</summary>
<p>
 
  Наборы представляют собой наборы значений, как и массивы, за исключением двух отличий:

    * Предметы хранятся не в каком-либо порядке; они хранятся в случайном порядке, поэтому мы не можем считывать значения из набора с использованием числовых позиций, как с массивами. 
    
  * Ни один предмет не может появляться в наборе дважды; все предметы должны быть уникальными.
  
  `let colors = Set(["red", "green", "blue"])`
  
    > Поскольку set не должен хранить ваши объекты в том порядке, в котором вы их добавляете, 
    > они вместо этого могут хранить их в случайном порядке, который оптимизирует их для быстрого поиска. 
    > Итак, когда вы говорите «содержит ли этот набор элемент X», вы получите ответ за доли секунды, независимо от того, насколько велик набор.

</p>
</details>

* dictionaries (словари) - неупорядоченная структура данных, которая позволяет хранить пары «ключ — значение». 


<details><summary>Open</summary>
<p>
  
  Словари - это коллекции значений, как и массивы, но вместо того, чтобы хранить вещи с целочисленной позицией, вы можете получить к ним доступ, используя все, что захотите.
 
  `let heights = ["Taylor Swift": 1.78, "Ed Sheeran": 1.73]` или `идентификатора(ключ) : значение, которое мы хотим сохранить`

   Получить значения: `let result: Int = heights["Taylor Swift", default: 0]`; default - значит, что есть значения "Taylor Swift" нет в словаре, то верни 0.
  
   > В отличие от кортежей, нельзя гарантировать, что ключ в словаре существует. 
   > Вот почему чтение значения из словаря может ничего не вернуть - возможно, вы запросили ключ, которого не существует!
  
</p>
</details>











