# Лабораторна 1: Розробка термінальної аплікації

## Основні положення

### Мета
Розробити аплікацію з термінальним інтерфейсом.

### Завдання
Обрати одну з задач або узгодити свою тему з викладачем. (Задачі внизу).

## Задачі

### Бики та корови

#### Задача
Комп'ютер задумує чотиризначне число, в якому не повторюються цифри (наприклад 1234, а 1223 не можна), а ви намагаєтесь його вгадати. Після кожної спроби комп'ютер повідомляє вам кількість цифр що збігаються і стоять на свому місці (бики) та кількість цифр що є в задуманому числі але стоять не на своєму місці (корови).

#### Приклад роботи програми
Комп'ютер задумав число `7241` (про це не повідомляється користувачу).
```
Спроба: 1234
Бики: 1; Корови: 2.
```
Один бик це 2 на другії позиції. Одна корова це 4, що стоїть на четвертій, а не на третій позиції. (Про це також не повідомляється користувачу).
```
Спроба: 7421
Бики: 2; Корови: 2.
Спроба: 7241
Це правильне число! Спроб: 3
```

#### Варіації
- Замість чисел можуть використовуватись букви;
- Користувач може задумувати число, а комп'ютер вгадувати.

#### [Посилання (укр.)](https://uk.wikipedia.org/wiki/%D0%91%D0%B8%D0%BA%D0%B8_%D1%82%D0%B0_%D0%BA%D0%BE%D1%80%D0%BE%D0%B2%D0%B8)

### Життя

#### Задача
Поле M на N вважається заповнене *клітинами*. Клітини можуть бути у двох станах *Живі* та *Мертві*. Перше покоління заповнюється користувачем або випадково. Кожне наступне покоління виводиться з попереднього за правилами:
- Якщо в живої клітини два або три сусіди - вона лишається жити;
- Якщо в живої клітини один або нуль сусідів - вона помирає від самотності;
- Якщо в живої клітини чотири або більше сусідів - вона помирає від перенаселення;
- Якщо в мертвої клітини рівно три сусіди - вона оживає.

#### Варіації
- Дати можливість на початку згенерувати одну з стійких фігур (див. посилання).

#### [Посилання (укр.)](https://uk.wikipedia.org/wiki/%D0%96%D0%B8%D1%82%D1%82%D1%8F_%28%D0%B3%D1%80%D0%B0%29)

### Змійка

#### Задача
На полі M на N користувач керує змійкою. Змійка рухаться сама в напрямку голови, користувач може лише змінювати напрямок. Випадковим чином на полі з'являються поживні речовини, посля споживання яких, довжина змійки збільшується на одиницю. Гра закінчується коли змія врізається в межі поля.

#### Варіації
- На полі можуть з'являтись непоживні речовини, які зменшують або вбивають змійку;
- Межі поля можуть бути складної форми;
- На полі можуть бути інші змії які можуть істи одна одну починаючи з хвоста.

#### [Посилання (en.)](https://en.wikipedia.org/wiki/Snake)

### Гомоку

#### Задача
Гравці по черзі ставлять хрестики і нулики на полі NxM. Виграє гравечь що поставить 5 хрестиків або нуликів підряд.

#### Варіації
- Одним гравцем може бути комп'ютер.

#### [Посилання (укр.)](https://uk.wikipedia.org/wiki/%D0%93%D0%BE%D0%BC%D0%BE%D0%BA%D1%83)

## Матеріали

### node

#### Запуск аплікації
```
node app.js
```

#### Запуск аплікації в режимі зневаждення
```
node inspect app.js
```

#### Запуск аплікації в режимі зневаждення з зовнішнім зневаджувачем
```
node --inspect app.js
```

#### Запуск аплікації в режимі зневаждення з зовнішнім зневаджувачем із зупинкою на першій стрічці
```
node --inspect-brk app.js
```

#### Приєднання зовнішнього зневаджувача Google Chrome
Перейдіть на адресу:
```
chrome://inspect
```

### npm

#### Ініціалізація нової аплікації
```
npm init
```

#### Додавання пакету
```
npm install --save package
```

#### Встановлення всіх доданих пакетів
```
npm install
```

### console

#### Вивід у термінал
```
console.log('Hello World!');
```

#### Очистка терміналу
```
console.clear();
```

**Зверніть увагу** у старіших версіях node.js необхідно використовувати вивід спеціального символу для очистки терміналу:
```
process.stdout.write('\033c');
```

#### Вивід у термінал сиволів без переводу рядка
```
process.stdout.write('Hello');
```
**Обережно! `process.stdout.write` вміє працювати тільки зі стрічками. Якщо ви хочете вивести число, необхідно привести його до стрічки за допомогою `toString()`.**

### readline-sync

#### Встановлення
```
npm install --save readline-sync
```

### Зчитування вводу користувача
```
const readlineSync = require('readline-sync');

const name = readlineSync.question('What is your name? ');
```

### Git

#### Ініціалізація
```
git init
```

#### Додавання файлів
```
git add FILE
```

#### Створення внеску (commit)
```
git commit -m "message"
```

#### Завантаження внеску на сервер
```
git push origin master
```