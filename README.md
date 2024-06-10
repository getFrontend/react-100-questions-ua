## Що таке React?

**React** - це бібліотека JavaScript, розроблена компанією Facebook, яка використовується для створення користувацьких інтерфейсів.

Вона дає змогу розбивати призначений для користувача інтерфейс на невеликі компоненти, які можуть оновлюватися незалежно один від одного, що забезпечує ефективне управління станом і оновленнями на веб-сторінці.

React використовує віртуальне DOM (Document Object Model) для оптимізації продуктивності, даючи змогу ефективно оновлювати тільки частини інтерфейсу, що змінилися.

Однією з головних концепцій React є "односпрямований потік даних", що полегшує відстеження змін і управління станом програми. React широко використовується в розробці веб-додатків і мобільних додатків з використанням фреймворка React Native.

## Які основні переваги використання React?

Використання React має кілька ключових переваг:

1. Віртуальний DOM: React використовує віртуальний DOM для ефективного управління оновленнями інтерфейсу. Це дає змогу мінімізувати операції безпосередньо з реальним DOM, що підвищує продуктивність програми.

2. Компонентний підхід: React дає змогу розбивати користувацький інтерфейс на безліч дрібних компонентів. Ці компоненти можуть бути повторно використані, що спрощує розробку, тестування та обслуговування коду.

3. Односпрямований потік даних: React забезпечує односпрямований потік даних, що спрощує відстеження змін стану і робить код більш передбачуваним і легко підтримуваним.

4. Оголошувальний підхід: React використовує оголошувальний стиль програмування, який дає змогу описувати, який вигляд має мати інтерфейс залежно від стану. Це робить код більш читабельним і зрозумілим.

5. Екосистема і співтовариство: React має велику й активну спільноту розробників, що забезпечує безліч готових рішень, бібліотек та інструментів для розробки.

6. React Native: Для розробки мобільних додатків можна використовувати React Native, який дає змогу використовувати React для створення нативних мобільних додатків під різні платформи.

7. Висока продуктивність: Завдяки віртуальному DOM і оптимізаціям, React здатний забезпечувати хорошу продуктивність навіть під час роботи з великими і складними інтерфейсами.

## Що таке JSX?

**JSX** (JavaScript XML) - це розширення синтаксису JavaScript, що використовується в React для опису структури користувацького інтерфейсу.

Цей синтаксис дає змогу об'єднувати код JavaScript і HTML-подібні елементи в одному місці, що робить створення компонентів React більш інтуїтивним і читабельним.

JSX дає змогу вставляти JavaScript-вирази всередині тегів, укладаючи їх у фігурні дужки. Наприклад:

```
const name = "Микола";
const element = <h1>Привіт, {name}</h1>;
```

У цьому прикладі змінна name вставлена всередині JSX-елемента за допомогою фігурних дужок.

JSX також дає змогу описувати користувацькі компоненти користувача у вигляді елементів, що робить код більш структурованим і зручним для читання:

```
function Greeting(props) {
  return <p>Привіт, {props.name}!</p>;
}
```

JSX-код потрібно перетворити на звичайний JavaScript-код перед тим, як він буде виконаний у браузері. Для цього використовуються інструменти компіляції, зазвичай включені в складальний процес проекту на React.

## Які основні відмінності між компонентами класів і функціональними компонентами в React?

У React існують два основні способи створення компонентів: з використанням класів і з використанням функціональних компонентів. Ось основні відмінності між ними:

### Компоненти класів:

1. Синтаксис: Компоненти класів визначаються як класи, що розширюють базовий клас React.Component.

2. Стан (state): Компоненти класів мають вбудовану підтримку для стану (state), що дає їм змогу зберігати та керувати даними всередині компонента.

3. Методи життєвого циклу: Компоненти класів мають широкий набір методів життєвого циклу (наприклад, componentDidMount, componentDidUpdate, componentWillUnmount), які дають змогу реагувати на різні етапи життя компонента.

4. Пропси (props): Пропси передаються в компоненти класів через атрибути під час використання. Вони доступні через this.props всередині методів компонента.

### Функціональні компоненти:

1. Синтаксис: Функціональні компоненти визначаються як звичайні функції.

2. Стан (state): Спочатку функціональні компоненти не підтримували стан. Однак із появою хуків (hooks) у React (починаючи з React 16.8) функціональні компоненти тепер можуть використовувати стан та інші можливості, що раніше були доступні тільки компонентам класів.

3. Хуки (hooks): Функціональні компоненти можуть використовувати хуки, як-от useState, useEffect та інші, для керування станом, ефектами та іншими аспектами.

4. Пропси (props): Пропси також передаються функціональним компонентам, але доступні вони як аргументи функції.

Загалом, з появою хуків, функціональні компоненти стали кращим вибором для більшості випадків у React, оскільки вони забезпечують простіший синтаксис, який можна прочитати, а також спрощений спосіб керування станом і ефектами.

## Що таке Virtual DOM, та як він працює?

Virtual DOM (віртуальне DOM) - це концепція, яку використовують у бібліотеках і фреймворках, як-от React, для оптимізації оновлень реального DOM (Document Object Model) і підвищення продуктивності веб-додатків.

Реальний DOM - це представлення структури веб-сторінки в браузері у вигляді дерева об'єктів. Коли стан програми змінюється і потрібне оновлення інтерфейсу, браузер виконує зміни безпосередньо в реальному DOM. Однак багаторазові та часті оновлення реального DOM можуть бути витратними з погляду продуктивності, особливо для великих і складних інтерфейсів.

Віртуальний DOM розв'язує цю проблему таким чином:

1. Створення віртуального DOM: Під час зміни стану застосунку React створює віртуальне представлення DOM-структури, яка є легковажною копією реального DOM.

2. Порівняння віртуального DOM: React порівнює попередній стан віртуального DOM із новим станом, виявляючи, які частини інтерфейсу було змінено.

3. Генерація різниці (патч): На основі порівняння React створює мінімальний набір змін, необхідних для оновлення віртуального DOM згідно з новим станом.

4. Застосування змін: Створені зміни застосовуються до реального DOM тільки одним оновленням, що дає змогу уникнути множинних маніпуляцій із реальним DOM.

Використання віртуального DOM дає змогу значно поліпшити продуктивність, оскільки оновлення реального DOM відбуваються тільки в необхідних місцях. Це також робить розробку більш зручною і передбачуваною, оскільки розробнику не потрібно вручну керувати безліччю змін на реальному DOM.

## Які методи життєвого циклу компонентів ви знаєте?

У React компоненти проходять через низку етапів свого "життєвого циклу", включно з такими методами:

1. **constructor(props)**: Викликається під час створення компонента. Тут відбувається ініціалізація стану і прив'язка методів.

2. **componentDidMount()**: Викликається після того, як компонент було вставлено в DOM. Часто використовується для завантаження даних із сервера.

3. **componentDidUpdate(prevProps, prevState)**: Викликається після оновлення компонента. Дозволяє реагувати на зміни пропсів або стану.

4. **shouldComponentUpdate(nextProps, nextState)**: Дозволяє оптимізувати оновлення компонента, повертаючи false, якщо оновлення не потрібне.

5. **componentWillUnmount()**: Викликається перед видаленням компонента з DOM. Використовується для очищення ресурсів.

6. **static getDerivedStateFromProps(props, state)**: Рідко використовується. Дозволяє оновити стан на основі нових пропсів.

7. **getSnapshotBeforeUpdate(prevProps, prevState)**: Рідко використовується. Дозволяє отримати інформацію з DOM перед його оновленням.

8. **componentDidCatch(error, info)**: Використовується для обробки помилок у дочірніх компонентах.

Це лише короткий огляд методів життєвого циклу компонентів у React.

## Що таке "стан" (state) компонента в React?

"Стан" (state) у React є об'єктом, який містить дані, що впливають на те, як компонент відображається і поводиться. Стан є одним із фундаментальних понять React і використовується для зберігання інформації, яка може змінюватися під час роботи програми.

Коли стан компонента змінюється, React автоматично перерендерує компонент, щоб відобразити новий стан. Стан зазвичай ініціалізується в методі constructor() компонента, і для його оновлення використовується метод setState().

Приклад:

```
import React, { Component } from "react";

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0, // Початковий стан
    };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>Счетчик: {this.state.count}</p>
        <button onClick={this.increment}>Збільшити</button>
      </div>
    );
  }
}

export default Counter;
```

У цьому прикладі компонент Counter має стан count, який оновлюється при кліці на кнопку. Під час виклику setState(), React оновить стан і перерендерить компонент, відображаючи нове значення count.

## Як оновити стан компонента?

У React для оновлення стану компонента слід використовувати метод setState(). Цей метод приймає або об'єкт з оновленнями стану, або функцію, яка повертає об'єкт з оновленнями. Під час виклику setState(), React оновить стан компонента і перерендерує його, щоб відобразити новий стан.

Приклад використання setState():

```
import React, { Component } from "react";

class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }

  increment = () => {
    //  Оновлення стану з використанням об'єкта
    this.setState({ count: this.state.count + 1 });
  };

  decrement = () => {
    // Оновлення стану з використанням функції
    this.setState((prevState) => {
      return { count: prevState.count - 1 };
    });
  };

  render() {
    return (
      <div>
        <p>Счетчик: {this.state.count}</p>
        <button onClick={this.increment}>Збільшити</button>
        <button onClick={this.decrement}>Зменшити</button>
      </div>
    );
  }
}

export default Counter;
```

У цьому прикладі increment() і decrement() оновлюють стан count за допомогою setState(). Важливо використовувати функції під час оновлення стану, особливо якщо новий стан залежить від попереднього стану, щоб уникнути проблем з асинхронністю.

## Что такое пропсы (props) в React?

"Пропси" (props) у React - це механізм передачі даних від батьківського компонента до дочірнього. Вони являють собою атрибути, які задаються при створенні компонента і не можуть бути змінені самим компонентом, який їх отримує. Пропси використовуються для передачі інформації про стан або конфігурацію компонента.

Приклад використання пропсів:

```
import React from "react";

function Welcome(props) {
  return <h1>Вітаю, {props.name}!</h1>;
}

const App = () => {
  return <Welcome name="Ірина" />;
};

export default App;
```

У цьому прикладі компонент **Welcome** приймає пропс **name** і використовує його для виведення персоналізованого привітання. Компонент **App** передає значення "Ірина" в пропс **name** компонента **Welcome**.

Пропси передаються у вигляді об'єкта і доступні як властивості (**props**) всередині дочірнього компонента.

Використання пропсів дає змогу створювати більш гнучкі та перевикористовувані компоненти, адже можна налаштовувати їхню поведінку та відображення ззовні.

## У чому різниця між станом і пропсами в React?

Стан (**state**) і пропси (**props**) - це два основні концепти в React, які використовуються для управління даними в компонентах. Вони мають різні цілі та характеристики:

#### Стан (state):

1. Стан - це внутрішні дані компонента, які можуть змінюватися під час виконання.
2. Визначається та керується самим компонентом, у якому він знаходиться.
3. Зміна стану викликає перерендеринг компонента, щоб відобразити новий стан.
4. Доступно тільки для компонента, у якому було визначено стан.
5. Оновлюється з використанням методу setState().

#### Пропсы (props):

1. Пропси - це дані, що передаються від батьківського компонента до дочірнього компонента.
2. Не можна змінити пропси всередині дочірнього компонента. Вони вважаються "тільки для читання".
3. Пропси слугують для налаштування та передавання даних у компоненти.
4. Використовуються для зв'язку між різними компонентами і передавання інформації вниз по ієрархії.
5. Не спричиняють перерендерінг у разі їхньої зміни.

Коротко кажучи, стан призначений для зберігання і управління даними, що змінюються всередині компонента, тоді як пропси призначені для передачі даних від батьківського компонента до дочірнього. Обидва ці концепти допомагають створювати динамічні та перевикористовувані інтерфейси в React додатках.

## Як обробляти події в React?

У React обробка подій відбувається з використанням синтаксису, аналогічного обробці подій у нативному JavaScript, але з деякими відмінностями. Ось як обробляти події в React:

1. Створення методу обробки події: Створіть метод усередині компонента, який буде виконуватися при виникненні події. Назва методу зазвичай починається з префікса "handle", за яким слідує ім'я події або описове ім'я.

2. Прив'язка методу до елемента: Прив'яжіть створений метод до елемента, який генеруватиме подію. Це робиться за допомогою JSX, вказавши метод як значення атрибута події.

3. Використання аргументів: Усередині методу обробки події ви можете отримати доступ до об'єкта події та використовувати його властивості, такі як `target`, щоб отримати інформацію про подію.

Приклад обробки кліка:

```
import React, { Component } from "react";

class Button extends Component {
  handleClick = () => {
    console.log("Кнопка була натиснута");
  };

  render() {
    return <button onClick={this.handleClick}>Натисни на мене</button>;
  }
}

export default Button;
```

В этом примере метод `handleClick` вызывается при клике на кнопку, выводя сообщение в консоль.

Важно заметить, что при передаче метода обработки события в качестве атрибута JSX, не следует вызывать его с помощью круглых скобок (например, не пишите `onClick={this.handleClick()}`), так как это вызовет выполнение метода сразу при рендеринге.

## Що таке умовний рендеринг у React?

Умовний рендеринг у React - це підхід, за якого вирішується, чи повинен компонент або його частина відображатися на основі будь-якої умови. Це дає змогу динамічно контролювати, які елементи інтерфейсу будуть показані або приховані залежно від стану застосунку або інших чинників.

Приклад умовного рендерингу:

```
import React, { Component } from "react";

class Greeting extends Component {
  render() {
    const isLoggedIn = this.props.isLoggedIn;

    if (isLoggedIn) {
      return <h1>Вітаємо вас на нашому сайті!</h1>;
    } else {
      return <h1>Будь ласка, увійдіть до системи!</h1>;
    }
  }
}

export default Greeting;
```

У цьому прикладі компонент Greeting залежно від значення пропса isLoggedIn рендерить різні заголовки. Якщо isLoggedIn дорівнює true, відображається привітання, в іншому разі - запрошення до входу в систему.

Умовний рендеринг можна реалізувати також за допомогою тернарного оператора:

```
class Greeting extends Component {
  render() {
    const isLoggedIn = this.props.isLoggedIn;

    return (
      <div>
        {isLoggedIn ? (
          <h1>Привіт, Сергій!</h1>
        ) : (
          <h1>Будь ласка, авторизуйтеся на сайті.</h1>
        )}
      </div>
    );
  }
}
```

Умовний рендеринг особливо корисний, коли потрібно адаптувати інтерфейс на основі динамічних даних або станів, таких як авторизація користувача, наявність даних та інші умови.

## Як передати дані між компонентами вгору і вниз за ієрархією?

У React дані можуть передаватися між компонентами вгору і вниз по ієрархії з використанням пропсів (props) і колбеків (callback функцій). Ось як це працює:

#### Передача даних вниз за ієрархією (від батька до дочірнього компонента):

Пропси (props): Батьківський компонент передає дані своєму дочірньому компоненту через пропси. Дочірній компонент може отримати доступ до цих даних як властивості (props).

Приклад:

```
// Батьківський компонент
import React from "react";
import ChildComponent from "./ChildComponent";

const ParentComponent = () => {
  const data = "Дані для дочірнього компонента";

  return <ChildComponent dataProp={data} />;
};

// Дочірній компонент
import React from "react";

const ChildComponent = (props) => {
  return <p>{props.dataProp}</p>;
};

export default ChildComponent;
```

#### Передавання даних вгору за ієрархією (від дочірнього компонента до батька):

Колбеки (callback функції): Батьківський компонент передає функцію як пропса дочірньому компоненту. Дочірній компонент може викликати цю функцію, передаючи їй дані назад вгору по ієрархії.

Приклад:

```
// Батьківський компонент
import React, { useState } from "react";
import ChildComponent from "./ChildComponent";

const ParentComponent = () => {
  const [receivedData, setReceivedData] = useState("");

  const handleDataChange = (data) => {
    setReceivedData(data);
  };

  return (
    <div>
      <p>Отримані дані: {receivedData}</p>
      <ChildComponent onDataChange={handleDataChange} />
    </div>
  );
};

// Дочірній компонент
import React from "react";

const ChildComponent = (props) => {
  const sendDataToParent = () => {
    props.onDataChange("Дані від дочірнього компонента");
  };

  return <button onClick={sendDataToParent}>Надіслати дані</button>;
};

export default ChildComponent;
```

Це дає змогу дочірньому компоненту впливати на дані та стан батьківського компонента.

Використовуючи цей підхід, ви можете ефективно передавати й оновлювати дані між компонентами вгору і вниз по ієрархії.

## Как выполнить HTTP-запросы в React?

Для выполнения HTTP-запросов в React обычно используются библиотеки, такие как axios или встроенный fetch. Вот как выполнить GET-запрос с использованием библиотеки axios:

1. Установите библиотеку axios с помощью npm или yarn:

```
npm install axios
```

або

```
yarn add axios
```

2. У компоненті, де ви хочете виконати HTTP-запит:

```
import React, { useState, useEffect } from "react";
import axios from "axios";

const DataFetching = () => {
  const [data, setData] = useState(null);
  const [isLoading, setIsLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    axios
      .get("https://api.example.com/data")
      .then((response) => {
        setData(response.data);
        setIsLoading(false);
      })
      .catch((error) => {
        setError(error.message);
        setIsLoading(false);
      });
  }, []); // Порожній масив залежностей, щоб запит виконався тільки один раз

  if (isLoading) {
    return <p>Завантаження...</p>;
  }

  if (error) {
    return <p>Error: {error}</p>;
  }

  return (
    <div>
      <h2>Fetched Data</h2>
      <pre>{JSON.stringify(data, null, 2)}</pre>
    </div>
  );
};

export default DataFetching;
```

У цьому прикладі ми використовуємо хук useState для управління станом даних, завантаження і помилок. Хук useEffect використовується для виконання HTTP-запиту під час монтування компонента. Залежно від результату запиту, ми оновлюємо стан для відображення даних, завантаження або помилки.

## Що таке контекст (context) у React і для чого він використовується?

Контекст (context) у React - це механізм, який дає змогу передавати дані глибоко вниз по ієрархії компонентів, минаючи пропси (props). Він використовується, коли певні дані потрібні в безлічі компонентів, і передача через кожен компонент стає незручною.

Контекст дає змогу створити «контекстне» оточення, в якому компоненти можуть отримувати доступ до даних без необхідності явно передавати їх через пропси. Це особливо корисно для глобальних даних, таких як дані автентифікації, теми оформлення та інші загальні стани.

Для створення контексту використовуються два елементи: провайдер (Provider) і споживач (Consumer).

Приклад використання контексту:

```
import React, { createContext, useContext } from "react";

// Створюємо контекст
const UserContext = createContext();

// Компонент, який постачає дані
const UserProvider = ({ children }) => {
  const user = { name: "Serhii", role: "developer" };

  return <UserContext.Provider value={user}>{children}</UserContext.Provider>;
};

// Компонент, що використовує контекст
const UserInfo = () => {
  const user = useContext(UserContext);

  return (
    <div>
      <p>Name: {user.name}</p>
      <p>Role: {user.role}</p>
    </div>
  );
};

// Головний компонент, який обертає додаток у провайдер даних
const App = () => {
  return (
    <UserProvider>
      <UserInfo />
    </UserProvider>
  );
};

export default App;
```

У цьому прикладі контекст UserContext використовується для передачі інформації про користувача від UserProvider до UserInfo, минаючи пропси. Компонент UserInfo використовує хук useContext, щоб отримати доступ до даних контексту.

Контекст слід використовувати обережно і тільки там, де це справді необхідно, оскільки це може ускладнити розуміння взаємодії компонентів і ускладнити налагодження.

## Як реалізувати PureComponent?

Щоб створити **PureComponent** у React, ви можете використовувати класи або функціональні компоненти з хуками.

1. З використанням класів:

```
import React, { PureComponent } from "react";

class MyPureComponent extends PureComponent {
  render() {
    return <div>{/* Код компоненту */}</div>;
  }
}

export default MyPureComponent;
```

2. З використанням функціональних компонентів і хуків:

```
import React, { memo } from "react";

const MyPureComponent = () => {
  return <div>{/* Код компоненту */}</div>;
};

export default memo(MyPureComponent);
```

Обидва варіанти **PureComponent** автоматично порівнюють пропси і стан, і перемальовують компонент тільки в разі змін даних. Це може істотно поліпшити продуктивність, уникаючи непотрібних перемальовок.

## Що таке ключі (keys) у списках React-елементів і навіщо вони потрібні?

У React, ключі (keys) - це спеціальні атрибути, які використовуються під час рендерингу списків компонентів або елементів. Вони допомагають React оптимізувати процес оновлення та перемальовування компонентів у списках.

Ключі призначаються кожному елементу в списку і мають бути унікальними серед своїх сусідніх елементів. Коли React оновлює список компонентів, він використовує ключі для визначення, які елементи були додані, видалені або змінені. Без ключів React буде перемальовувати і оновлювати всі елементи в списку, що може призвести до погіршення продуктивності.

Приклад використання ключів:

```
import React from "react";

const TodoList = ({ data }) => {
  return (
    <ul>
      {data.map((todo) => (
        <li key={todo.id}>{todo.text}</li>
      ))}
    </ul>
  );
};

export default TodoList;
```

У цьому прикладі кожному елементу списку завдань (todo) присвоюється унікальний ключ (todo.id). Це дає змогу React ефективно оновлювати тільки змінені елементи, мінімізуючи кількість перемальовок.

Ключі особливо важливі під час роботи зі списками, які можуть змінюватися в часі, наприклад, під час додавання, видалення або переупорядкування елементів.

## Як використовувати стилі в React-компонентах?

У React для стилізації компонентів можна використовувати кілька підходів: вбудовані стилі (inline styles), стилі з використанням CSS-класів і бібліотеки стилів. Ось як це робиться:

#### 1. Вбудовані стилі (Inline Styles):

Вбудовані стилі являють собою об'єкт JavaScript, де ключі - це назви CSS-властивостей, а значення - відповідні значення властивостей.

```
import React from "react";

const MyComponent = () => {
  const styles = {
    backgroundColor: "blue",
    color: "yellow",
    padding: "12px",
    borderRadius: "20px",
  };

  return <div style={styles}>Стилізований компонент</div>;
};

export default MyComponent;
```

#### 2. Стилі з використанням CSS-класів:

Ви можете визначити CSS-класи в окремих файлах і додати їх до елементів у компонентах.

```
// styles.css
.myClass {
  background-color: blue;
  color: yellow;
  padding: 12px;
  border-radius: 20px;
}

// MyComponent.jsx
import React from 'react';
import './styles.css';

const MyComponent = () => {
  return <div className="myClass">Стилізований компонент</div>;
};

export default MyComponent;
```

#### 3. Бібліотеки стилів:

Існує безліч бібліотек для стилізації React-компонентів, таких як Styled Components, Emotion, CSS Modules та інші. Ці бібліотеки надають синтаксис для створення компонентів зі стилями всередині коду.

```
// Styled Components
import React from "react";
import styled from "styled-components";

const StyledDiv = styled.div`
  background-color: blue;
  color: yellow;
  padding: 12px;
  border-radius: 20px;
`;

const MyComponent = () => {
  return <StyledDiv>Стилізований компонент</StyledDiv>;
};

export default MyComponent;
```

Вибір методу залежить від уподобань та вимог проєкту. Важливо звернути увагу на підтримку класів, перевикористання стилів і простоту супроводу під час вибору підходу.

## Що таке «керовані компоненти» (controlled components)?

«Керовані компоненти» (controlled components) - це поняття, пов'язане з управлінням станом форм і введення даних у React. У керованих компонентах значення елемента введення (наприклад, текстового поля або чекбокса) контролюється станом React компонента, а не DOM елементом.

Коли компонент контролює значення введення, він зберігає це значення у своєму стані й оновлює його за допомогою обробників подій (наприклад, у разі зміни тексту в полі введення). Це дає змогу мати повний контроль над даними форми та легко реагувати на зміни.

Приклад керованого компонента з текстовим полем:

```
import React, { useState } from "react";

const ControlledComponent = () => {
  const [inputValue, setInputValue] = useState("");

  const handleInputChange = (event) => {
    setInputValue(event.target.value);
  };

  return (
    <div>
      <input type="text" value={inputValue} onChange={handleInputChange} />
      <p>Введене значення: {inputValue}</p>
    </div>
  );
};

export default ControlledComponent;
```

У цьому прикладі значення текстового поля inputValue пов'язане зі станом компонента. Коли значення текстового поля змінюється, викликається обробник handleInputChange, який оновлює стан і, отже, значення текстового поля.

Використання керованих компонентів забезпечує передбачуваність стану, спрощує взаємодію з даними і дає змогу виконувати валідацію та інші операції над введеними даними перед їхнім надсиланням на сервер.

## Що таке «некеровані компоненти» (uncontrolled components)?

«Некеровані компоненти» (uncontrolled components) - це поняття, протилежне керованим компонентам, і воно відноситься до управління станом форм і введення даних у React. У разі некерованих компонентів, значення елемента введення (наприклад, input або textarea) зберігається безпосередньо в DOM, і React компонент не керує цим значенням.

Замість використання стану компонента для зберігання значення елемента введення, некеровані компоненти звертаються до DOM безпосередньо для отримання та оновлення значення.

Приклад некерованого компонента з текстовим полем:

```
import React, { useRef } from "react";

const UncontrolledComponent = () => {
  const inputRef = useRef(null);

  const handleButtonClick = () => {
    alert("Значення в полі введення: " + inputRef.current.value);
  };

  return (
    <div>
      <input type="text" ref={inputRef} />
      <button onClick={handleButtonClick}>Показати значення</button>
    </div>
  );
};

export default UncontrolledComponent;
```

У цьому прикладі значення текстового поля не зберігається в стані компонента. Натомість ми використовуємо useRef для отримання посилання на DOM-елемент і потім отримуємо його значення через inputRef.current.value.

Некеровані компоненти можуть бути корисними, коли у вас є особливі випадки або вимоги, де контроль над станом через React не є оптимальним підходом. Однак, у більшості випадків, керовані компоненти забезпечують більш передбачуване і зручне управління даними у формах.

## Що таке «підйом стану» (lifting state up)?

«Підйом стану» (lifting state up) - це патерн у React, який передбачає переміщення стану з дочірніх компонентів до батьківських компонентів, щоб розділяти й керувати станом на вищому рівні та передавати його через пропси.

Цей підхід особливо корисний, коли кілька компонентів повинні мати доступ до одного й того самого стану або коли стан повинен бути синхронізований між різними частинами програми.

Приклад із підйомом стану:

```
import React, { useState } from "react";

const TemperatureInput = ({ scale, temperature, onTemperatureChange }) => {
  return (
    <fieldset>
      <legend>Введіть температуру в градусах {scale}:</legend>
      <input
        value={temperature}
        onChange={(e) => onTemperatureChange(e.target.value)}
      />
    </fieldset>
  );
};

const Calculator = () => {
  const [celsius, setCelsius] = useState("");
  const [fahrenheit, setFahrenheit] = useState("");

  const handleCelsiusChange = (value) => {
    setCelsius(value);
    setFahrenheit((value * 9) / 5 + 32);
  };

  const handleFahrenheitChange = (value) => {
    setFahrenheit(value);
    setCelsius(((value - 32) * 5) / 9);
  };

  return (
    <div>
      <TemperatureInput
        scale="C"
        temperature={celsius}
        onTemperatureChange={handleCelsiusChange}
      />
      <TemperatureInput
        scale="F"
        temperature={fahrenheit}
        onTemperatureChange={handleFahrenheitChange}
      />
    </div>
  );
};

export default Calculator;
```

У цьому прикладі компонент Calculator піднімає стан температур із TemperatureInput компонентів. При зміні температури в одному з вводів, стан піднімається в батьківський компонент Calculator, який потім оновлює стан для іншого вводу, забезпечуючи синхронізацію температур в обох шкалах.

«Підйом стану» допомагає спростити керування даними та їхню синхронізацію між компонентами, особливо під час роботи з компонентами на різних рівнях ієрархії.

## Як створити форму в React?

Створення форми в React охоплює використання HTML-елементів форми в JSX і управління введенням даних за допомогою стану. Ось як це робиться:

#### Створення компонента форми:

Спочатку створіть компонент форми і визначте елементи форми всередині нього, такі як текстові поля, чекбокси, кнопки тощо.

```
import React, { useState } from "react";

const MyForm = () => {
  const [formData, setFormData] = useState({
    name: "",
    email: "",
    // інші поля форми
  });

  const handleInputChange = (event) => {
    const { name, value } = event.target;
    setFormData({
      ...formData,
      [name]: value,
    });
  };

  const handleSubmit = (event) => {
    event.preventDefault();
    console.log(formData);
    // відправляємо дані на сервер або виконуємо інші операції
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
          Ім&apos;я:
        <input
          type="text"
          name="name"
          value={formData.name}
          onChange={handleInputChange}
        />
      </label>
      <br />
      <label>
        Email:
        <input
          type="email"
          name="email"
          value={formData.email}
          onChange={handleInputChange}
        />
      </label>
      <br />
      {/* Інші поля форми  */}
      <button type="submit">Отправить</button>
    </form>
  );
};

export default MyForm;
```

#### Управління станом:

У цьому прикладі використовується хук useState, щоб керувати станом даних форми. Обробник handleInputChange викликається при зміні полів введення і оновлює стан форми.

#### Обробка надсилання:

Обробник handleSubmit викликається під час надсилання форми. У цьому випадку ми запобігаємо стандартній поведінці надсилання форми на сервер за допомогою event.preventDefault(), щоб продемонструвати обробку даних на клієнті.

#### Прив'язка значень до полів:

Значення полів форми пов'язані зі станом форми. value елементів введення встановлюється рівним значенням зі стану, а при зміні полів викликається обробник handleInputChange.

#### Надсилання даних:

Після заповнення форми і натискання кнопки відправлення, дані можна використовувати для відправлення на сервер, виконання операцій або інших необхідних дій.

## Як реалізувати умовне додавання класу до елемента в React?

У React ви можете умовно додати клас до елемента, використовуючи тернарний оператор або функцію для визначення класового імені. Ось приклади обох підходів:

#### З використанням тернарного оператора:

```
import React from "react";

const MyComponent = ({ isActive }) => {
  return (
    <div className={isActive ? "active" : "inactive"}>
      Вміст компонента
    </div>
  );
};

export default MyComponent;
```

У цьому прикладі клас active буде додано до елемента, якщо isActive дорівнює true, інакше буде додано клас inactive.

#### З використанням функції для визначення класу:

```
import React from "react";

const MyComponent = ({ isActive }) => {
  const getClassNames = () => {
    return isActive ? "active" : "inactive";
  };

  return <div className={getClassNames()}>Вміст компонента</div>;
};

export default MyComponent;
```

Тут ми визначаємо функцію getClassNames, яка повертає клас залежно від значення isActive.

Якщо ви хочете додати кілька класів, ви можете використовувати об'єднання рядків або бібліотеки, такі як classnames.

```
import React from "react";
import classnames from "classnames";

const MyComponent = ({ isActive, isHighlighted }) => {
  const classNames = classnames({
    active: isActive,
    highlighted: isHighlighted,
  });

  return <div className={classNames}>Вміст компонента</div>;
};

export default MyComponent;
```

У цьому прикладі classnames бібліотека дає змогу додати кілька класів на основі об'єкта, де ключі - це назви класів, а значення - умови, за яких клас буде додано.

## Що таке фрагменти (fragments) у React?

Фрагменти (fragments) - це механізм у React, який дає змогу вам групувати дочірні елементи без необхідності створювати зайві DOM-елементи. Вони дають змогу повернути кілька елементів із компонента без обертання їх у додатковий DOM-контейнер.

До появи фрагментів, якщо ви хотіли повернути кілька елементів із компонента, вам доводилося обгортати їх у додатковий елемент (наприклад, <div>) або використовувати масив, що могло призвести до зайвого рівня вкладеності або проблем із CSS.

З використанням фрагментів, це має чистіший і ефективніший вигляд:

```
import React from "react";

const MyComponent = () => {
  return (
    <>
      <div>Блок 1</div>
	  <div>Блок 2</div>
    </>
  );
};

export default MyComponent;
```

Фрагменти можуть бути оголошені за допомогою порожніх <> і </>, а всередині них ви можете розміщувати будь-яку кількість дочірніх елементів.

Фрагменти особливо корисні, коли вам потрібно повернути кілька елементів з компонента, наприклад, з умовних блоків або маппінгу масивів, і ви хочете уникнути створення додаткових контейнерів у DOM.

## Яким чином можна оптимізувати продуктивність React-додатку?

Оптимізація продуктивності React-додатку - це важливий аспект, який може суттєво вплинути на користувацький досвід. Ось деякі способи оптимізації продуктивності:

1. Використовуйте керовані компоненти:

Використовуйте керовані компоненти для контролю над даними у формах і введенні. Це дасть змогу мінімізувати непотрібні перемальовування і полегшить обробку введених даних.

2. Використовуйте ключі (keys) правильно:

Під час рендерингу списків компонентів переконайтеся, що в кожного елемента є унікальний ключ. Це дасть змогу React ефективно оновлювати тільки змінені елементи.

3. Ледаче завантаження (Code Splitting):

Розділіть ваш застосунок на невеликі фрагменти і використовуйте механізм ледачого завантаження для завантаження компонентів тільки тоді, коли вони дійсно потрібні.

4. Мемоїзація:

Використовуйте хуки useMemo та useCallback для кешування обчислень і уникнення непотрібних перерахунків під час рендерингу.

5. Пакети компонентів (Component Libraries):

Використовуйте готові пакети компонентів (наприклад, Material-UI, Ant Design), які оптимізовані та протестовані з урахуванням продуктивності.

6. Віртуалізація списків:

Під час роботи з великими списками даних використовуйте бібліотеки віртуалізації (наприклад, react-virtualized), щоб рендерити тільки видимі елементи списку.

7. Оптимізація рендерінгу:

Уникайте непотрібних рендерів компонентів, використовуйте shouldComponentUpdate (у класових компонентах) або React.memo (у функціональних компонентах) для запобігання зайвим перемальовуванням.

8. Уникайте глибокої вкладеності:

Постарайтеся не створювати надто глибоку ієрархію компонентів, щоб зменшити час рендерингу та перерахунку.

9. Аналіз продуктивності:

Використовуйте інструменти, як-от React DevTools та браузерні інструменти продуктивності, щоб аналізувати й оптимізувати продуктивність вашого застосунку.

10. Серверний рендеринг (Server-Side Rendering, SSR):

Якщо це доречно для вашого застосунку, розгляньте можливість використання SSR для поліпшення початкового завантаження та SEO.

Зверніть увагу, що оптимізація продуктивності залежить від конкретного контексту вашого застосунку. Рекомендується використовувати інструменти профілювання та вимірювати продуктивність після кожної оптимізації, щоб переконатися, що вона справді призводить до поліпшень.

## Що таке HOC (Higher-Order Component) у React?

Високорівневий компонент (Higher-Order Component, HOC) - це патерн у React, який дає змогу повторно використовувати логіку компонентів, абстрагуючи її від самих компонентів. HOC не є частиною API React, це радше патерн композиції компонентів.

HOC - це функція, яка приймає компонент і повертає новий компонент із додатковою логікою. HOC дають змогу винести загальні функціональні або структурні аспекти компонентів і повторно використовувати їх із різними компонентами.

Приклад HOC:

```
import React from "react";

const withLogger = (WrappedComponent) => {
  return class WithLogger extends React.Component {
    componentDidMount() {
      console.log("Рендерінг компонента");
    }

    render() {
      return <WrappedComponent {...this.props} />;
    }
  };
};

const MyComponent = () => {
  return <div>Вміст компонента</div>;
};

const EnhancedComponent = withLogger(MyComponent);

export default EnhancedComponent;
```

У цьому прикладі withLogger - це HOC, який додає логування в метод componentDidMount. Потім компонент MyComponent обгортається HOC, створюючи EnhancedComponent.

HOC дозволяє:

- Розширювати функціональність компонентів без зміни самих компонентів.
- Перевикористовувати код і логіку між різними компонентами.
- Створювати загальні патерни для логування, аутентифікації, обробки помилок та інших аспектів.

Однак, з розвитком React і появою хуків, частина функціональності HOC тепер може бути реалізована з використанням хуків, таких як useEffect, useContext та інших. У більшості випадків, використання хуків є кращим.
