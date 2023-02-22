# JavaScript:
* __Объекты Встроенные методы.__
  * Знать методы статических объектов
  * Флаги и дескрипторы свойств (студент может установить свойство через Object.defineProperty)
  * Знать, как создавать итерируемые объекты, использовать Symbol.iterator(optional)

* __Типы данных и выражения ECMAScript__


  * Вычисляемые реквизиты объекта

    (__Object computed props__)

    *Вычисляемые свойства позволяют использовать значения выражений в качестве имен свойств объекта.*

    Было ранее
    ``` javascript
    function createObject(key, value) {
      let newObject = {};
      newObject[key] = value;
      return newObject;
    }
    createObject('car', 'Audi');
    // получаем объект { car: 'Audi' }
    ```

    ES6
    ```javascript
    function createObject(key, value) {
      return {
        [key]: value,
      };
    }
    createObject('car', 'Audi');
    // получаем объект { car: 'Audi' }

    ```


  * Be able to loop through Object keys

    (__Be able to loop through Object keys__)

  ***Как перебирать объекты в JavaScript?***

    Различные методы, которые можно использовать для перебора объектов в JavaScript:

  1. Использование цикла for...in
    ```javascript
    for (const key in user) {

    console.log(`${key}: ${user[key]}`);
    }
    ```

  2. Метод Object.keys
    ```javascript
    const keys = Object.keys(courses);
    // print all keys
    console.log(keys);
    // [ 'java', 'javascript', 'nodejs', 'php' ]
    // iterate over object
    keys.forEach((key, index) => {
        console.log(`${key}: ${courses[key]}`);
    });
    ```
  3. Метод Object.values

   Он возвращает значения всех свойств объекта в виде массива. Затем вы можете выполнить цикл по массиву значений, используя любой из методов цикла массива.
  ```javascript
  const animals = {
      tiger: 1,
      cat: 2,
      monkey: 3,
      elephant: 4
  };
  // iterate over object values
  Object.values(animals).forEach(val => console.log(val));
  ```

  4. Метод Object.entries

  Object.entries() выводит массив массивов, каждый из которых содержит два элемента. Первый элемент — это свойство, а второй — значение.

  ```javascript
  const animals = {
    tiger: 1,
    cat: 2,
    monkey: 3,
    elephant: 4
  };

  const entries = Object.entries(animals);
  console.log(entries);

  // [ [ 'tiger', 1 ],

  //   [ 'cat', 2 ],

  //   [ 'monkey', 3 ],

  //   [ 'elephant', 4 ] ]
  ```
  Чтобы перебрать массив, возвращаемый Object.entries(), вы можете использовать либо цикл for...of, либо метод forEach(), как показано ниже.ниже:

  ```javascript
  // `for...of` loop
  for (const [key, value] of Object.entries(animals)) {
      console.log(`${key}: ${value}`);
  }

  // `forEach()` method
  Object.entries(animals).forEach(([key, value]) => {
      console.log(`${key}: ${value}`)
  });
  ```

* __Functional Scope__
  * Know global scope and functional scope
    * *Глобальная область*: область по умолчанию для всего кода, работающего в режиме сценария.
    * *Область модуля*: область действия кода, работающего в модульном режиме.
    * *Область действия функции*: область действия, созданная с помощью функции .

* __Знать переменные зоны видимости__

  (__Know variables visibility areas__)

  Четыре сферы:

  1. Глобальный - виден всем
  2. Функция - видна внутри функции (и ее подфункций и блоков)
  3. Блок - виден внутри блока (и его подблоков)
  4. Модуль - виден внутри модуля

* __Понять вложенные области и способны работать с ними__
(__Understand nested scopes and able work with them__)

*