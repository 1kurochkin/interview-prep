<h3>
  <img src="../assets/React.png" width="16" height="16" />
  <span>React:</span>
</h3>

<details>
  <summary>Что такое React?</summary>
  <ul>
    <li>React — это JavaScript-библиотека для построения пользовательских интерфейсов</li>
    <li>Основная идея: разбивка UI на независимые компоненты</li>
    <li>Поддерживает декларативный стиль, Virtual DOM и компонентный подход</li>
  </ul>
</details>

<details>
  <summary>Перечислите особенности React?</summary>
  <ul>
    <li>Virtual DOM для оптимизации рендера</li>
    <li>Компонентный подход</li>
    <li>Поддержка JSX</li>
    <li>Односторонний поток данных</li>
    <li>Хуки для управления состоянием и жизненным циклом</li>
    <li>SSR (через ReactDOMServer)</li>
    <li>Поддержка мобильной разработки через React Native</li>
  </ul>
</details>

<details>
  <summary>Что такое Virtual DOM? Как он работает с React?</summary>
  <ul>
    <li>Virtual DOM — это легковесное представление реального DOM в памяти</li>
    <li>React обновляет Virtual DOM при изменении состояния</li>
    <li>Алгоритм сравнения (diffing) определяет минимальные изменения</li>
    <li>Только изменённые части обновляются в реальном DOM</li>
  </ul>
</details>

<details>
  <summary>Для чего нужен атрибут key при рендере списков?</summary>
  <ul>
    <li>Key помогает React отслеживать элементы при изменении списка</li>
    <li>Используется для оптимизации diffing-алгоритма</li>
    <li>Ключи должны быть уникальными среди соседних элементов</li>
    <li>Если не использовать key, возможны баги при рендере списков</li>
  </ul>
</details>

<details>
  <summary>Что такое PureComponent?</summary>
  <ul>
    <li>PureComponent — это компонент, который реализует поверхностное сравнение пропсов и состояния</li>
    <li>Предотвращает лишние рендеры</li>
    <li>Аналогично shouldComponentUpdate с shallow comparison</li>
    <li>Подходит, если пропсы и состояние — простые структуры</li>
  </ul>
</details>

<details>
  <summary>Что такое Компонент высшего порядка (Higher-Order Component/HOC)?</summary>
  <ul>
    <li>HOC — это функция, которая принимает компонент и возвращает новый компонент</li>
    <li>Используется для повторного использования логики</li>
    <li>Примеры: withRouter, connect из Redux</li>
    <li>Недостаток: «обёртывание в обёртку» (wrapper hell)</li>
  </ul>
</details>

<details>
  <summary>Разница между управляемыми (controlled) и не управляемыми (uncontrolled) компонентами?</summary>
  <ul>
    <li><b>Controlled:</b> состояние формы хранится в React (через state)</li>
    <li><b>Uncontrolled:</b> состояние хранится в DOM (доступ через ref)</li>
    <li>Controlled удобнее для валидации и синхронизации</li>
    <li>Uncontrolled проще для простых форм</li>
  </ul>
</details>

<details>
  <summary>Методы жизненного цикла компонента в React?</summary>
  <ul>
    <li><b>Mounting:</b> constructor, render, componentDidMount</li>
    <li><b>Updating:</b> shouldComponentUpdate, render, componentDidUpdate</li>
    <li><b>Unmounting:</b> componentWillUnmount</li>
    <li><b>Error handling:</b> componentDidCatch</li>
  </ul>
</details>

<details>
  <summary>Стадии жизненного цикла компонента в React?</summary>
  <ul>
    <li>Mounting (монтирование)</li>
    <li>Updating (обновление)</li>
    <li>Unmounting (размонтирование)</li>
    <li>Error handling (обработка ошибок)</li>
  </ul>
</details>

<details>
  <summary>Что такое React Reconciliation?</summary>
  <ul>
    <li>Алгоритм, с помощью которого React определяет, какие части UI нужно обновить</li>
    <li>Использует Virtual DOM и diffing</li>
    <li>Работает на уровне элементов, сравнивая деревья</li>
  </ul>
</details>

<details>
  <summary>Что такое портал (Portal)?</summary>
  <ul>
    <li>Способ рендера дочерних компонентов в другой DOM-узел вне иерархии родителя</li>
    <li>Используется для модалок, всплывающих подсказок</li>
    <li><code>ReactDOM.createPortal(child, container)</code></li>
  </ul>
</details>

<details>
  <summary>Что такое контекст (Context)?</summary>
  <ul>
    <li>Механизм передачи данных через дерево компонентов без пропсов</li>
    <li>Используется для глобальных данных (тема, язык, авторизация)</li>
    <li>API: React.createContext(), Provider, Consumer, useContext</li>
  </ul>
</details>

<details>
  <summary>Что такое React хуки (Hooks)?</summary>
  <ul>
    <li>Функции, которые позволяют использовать состояние и lifecycle в функциональных компонентах</li>
    <li>useState, useEffect, useContext, useReducer и др.</li>
    <li>Упрощают повторное использование логики</li>
  </ul>
</details>

<details>
  <summary>Что Такое JSX?</summary>
  <ul>
    <li>JSX — синтаксическое расширение JavaScript</li>
    <li>Позволяет писать HTML-подобный код внутри JS</li>
    <li>Преобразуется в React.createElement()</li>
    <li>Удобен для описания UI декларативно</li>
  </ul>
</details>

<details>
  <summary>Разница между JSX и HTML?</summary>
  <ul>
    <li>JSX = JavaScript с HTML-подобным синтаксисом</li>
    <li>В JSX используются className вместо class, htmlFor вместо for</li>
    <li>Все выражения пишутся в фигурных скобках {}</li>
    <li>JSX компилируется в JS-функции</li>
  </ul>
</details>

<details>
  <summary>Разница между состоянием (state) и пропсами (props)?</summary>
  <ul>
    <li>Props: внешние данные, передаваемые в компонент</li>
    <li>State: внутренние данные компонента</li>
    <li>Props неизменяемы внутри компонента</li>
    <li>State изменяется через setState / useState</li>
  </ul>
</details>

<details>
  <summary>Что такое React Fiber?</summary>
  <ul>
    <li>React Fiber — это новый алгоритм согласования (reconciliation)</li>
    <li>Позволяет разбивать рендер на части и приостанавливать его</li>
    <li>Обеспечивает приоритет обновлений (асинхронный рендеринг)</li>
    <li>Введён в React 16</li>
  </ul>
</details>

<details>
  <summary>Что такое фрагмент (Fragment)? Почему фрагмент лучше, чем div?</summary>
  <ul>
    <li>Fragment позволяет группировать элементы без добавления лишнего DOM-узла</li>
    <li>Синтаксис: <code>&lt;&gt;...&lt;/&gt;</code> или <code>React.Fragment</code></li>
    <li>Лучше, чем <code>div</code>, так как не нарушает семантику и структуру DOM</li>
  </ul>
</details>

<details>
  <summary>Что такое синтетические события в React?</summary>
  <ul>
    <li><code>SyntheticEvent</code> — обёртка над нативными событиями браузера</li>
    <li>Работает одинаково во всех браузерах</li>
    <li>Объединяет все события в единую систему React</li>
    <li>События автоматически переиспользуются (event pooling)</li>
  </ul>
</details>

<details>
  <summary>Что такое React-ссылка (ref)? Как создать ссылку?</summary>
  <ul>
    <li>Ref — способ получить доступ к DOM-элементу или экземпляру компонента</li>
    <li>Создание: <code>const ref = React.createRef()</code> или <code>useRef()</code></li>
    <li>Привязка: <code>&lt;input ref=&#123;ref&#125; /&gt;</code></li>
    <li>Доступ: <code>ref.current</code></li>
  </ul>
</details>

<details>
  <summary>Разница между теневым (Shadow) и виртуальным (Virtual) DOM?</summary>
  <ul>
    <li><strong>Shadow DOM</strong>: технология браузера для изоляции стилей и разметки в Web Components</li>
    <li><strong>Virtual DOM</strong>: структура данных React для оптимизации обновлений</li>
    <li>Shadow DOM = инкапсуляция; Virtual DOM = оптимизация</li>
  </ul>
</details>

<details>
  <summary>Назовите преимущества использования React?</summary>
  <ul>
    <li>Высокая производительность (Virtual DOM)</li>
    <li>Компонентный подход</li>
    <li>Богатая экосистема</li>
    <li>SSR и мобильные приложения (React Native)</li>
    <li>Большое сообщество и поддержка Facebook</li>
  </ul>
</details>

<details>
  <summary>Что такое условный рендеринг (Conditional Rendering)? Как его выполнить?</summary>
  <ul>
    <li>Отображение компонента в зависимости от условия</li>
    <li>Способы: оператор <code>if</code>, тернарный оператор <code>?:</code>, <code>&&</code></li>
    <li>Пример: <code>&#123;isLoggedIn ? &lt;Profile/&gt; : &lt;Login/&gt;&#125;</code></li>
  </ul>
</details>

<details>
  <summary>Что такое компонент-переключатель (Switching Component)?</summary>
  <ul>
    <li>Компонент, который выбирает и рендерит только один из вложенных компонентов</li>
    <li>Пример: <code>Switch</code> из React Router</li>
    <li>Удобен для маршрутизации</li>
  </ul>
</details>

<details>
  <summary>Разница между React и ReactDOM?</summary>
  <ul>
    <li>React: ядро для описания компонентов и логики</li>
    <li>ReactDOM: рендеринг компонентов в DOM</li>
    <li>React можно использовать и без браузера (например, React Native)</li>
  </ul>
</details>

<details>
  <summary>Разница между компонентом и контейнером?</summary>
  <ul>
    <li>Компонент: отвечает за отображение UI</li>
    <li>Контейнер: управляет логикой, состоянием, запросами к API</li>
    <li>Контейнер может передавать данные в компонент через props</li>
  </ul>
</details>

<details>
  <summary>Как React обрабатывает, или ограничивает использование пропсов определенного типа?</summary>
  <ul>
    <li>С помощью PropTypes или TypeScript</li>
    <li>PropTypes: встроенная библиотека для валидации типов</li>
    <li>TypeScript: строгая типизация на этапе разработки</li>
  </ul>
</details>

<details>
  <summary>Что такое строгий режим в React? Его преимущества?</summary>
  <ul>
    <li><code>StrictMode</code> — инструмент для выявления потенциальных проблем</li>
    <li>Проверяет небезопасные методы жизненного цикла</li>
    <li>Предупреждает о проблемах с хуками</li>
    <li>Не влияет на продакшен</li>
  </ul>
</details>

<details>
  <summary>Что такое «бурение пропсов» (Prop Drilling)? Как его избежать?</summary>
  <ul>
    <li>Передача пропсов через несколько уровней компонентов, даже если они нужны глубже</li>
    <li>Минусы: усложняет код</li>
    <li>Решение: Context API, Redux, Zustand, Recoil</li>
  </ul>
</details>

<details>
  <summary>Что такое «опрос» (Polling)? Как его реализовать в React?</summary>
  <ul>
    <li>Периодический запрос данных на сервер</li>
    <li>Реализация: <code>setInterval</code> + fetch/Axios</li>
    <li>Очистка интервала в <code>useEffect</code> при размонтировании</li>
  </ul>
</details>

<details>
  <summary>Разница между элементом и компонентом?</summary>
  <ul>
    <li>Элемент: простое описание UI (объект, возвращаемый из JSX)</li>
    <li>Компонент: функция или класс, который возвращает элементы</li>
    <li>Элемент статичен, компонент динамичен</li>
  </ul>
</details>

<details>
  <summary>Что такое ReactDOMServer?</summary>
  <ul>
    <li>Модуль для серверного рендеринга React-компонентов</li>
    <li>Методы: <code>renderToString()</code>, <code>renderToStaticMarkup()</code></li>
    <li>Используется для SEO и SSR</li>
  </ul>
</details>

<details>
  <summary>Что такое предохранители (Error Boundaries)?</summary>
  <ul>
    <li>Компоненты, которые перехватывают ошибки в дочерних компонентах</li>
    <li>Реализуются через <code>componentDidCatch</code> и <code>static getDerivedStateFromError</code></li>
    <li>Предотвращают падение всего приложения</li>
  </ul>
</details>

<details>
  <summary>Что такое «ленивая» (Lazy) функция?</summary>
  <ul>
    <li><code>React.lazy()</code> загружает компонент динамически (код-сплиттинг)</li>
    <li>Используется с <code>Suspense</code> для отображения fallback</li>
    <li>Улучшает производительность за счёт загрузки по требованию</li>
  </ul>
</details>

<details>
  <summary>Разница между рендерингом и монтированием?</summary>
  <ul>
    <li>Рендеринг: процесс генерации виртуального DOM</li>
    <li>Монтирование: добавление сгенерированного DOM в реальное дерево</li>
    <li>Рендеринг может происходить без монтирования (например, при SSR)</li>
  </ul>
</details>

<details>
  <summary>Что такое children?</summary>
  <ul>
    <li>Специальный пропс, который содержит вложенные элементы</li>
    <li>Пример: <code>&lt;Component&gt;Контент&lt;/Component&gt;</code> → <code>props.children = "Контент"</code></li>
    <li>Используется для компоновки компонентов</li>
  </ul>
</details>

<details>
  <summary>Что такое события указателя (Pointer Events)?</summary>
  <ul>
    <li>Универсальные события для мыши, касаний, пера</li>
    <li>React поддерживает <code>onPointerDown</code>, <code>onPointerMove</code>, <code>onPointerUp</code></li>
    <li>Объединяют разные типы ввода в единый API</li>
  </ul>
</details>

<details>
  <summary>Что такое инверсия наследования (Inheritance Inversion)?</summary>
  <ul>
    <li>Техника HOC, когда дочерний компонент контролирует рендеринг родителя</li>
    <li>Используется для внедрения логики или UI-модификаций</li>
    <li>Реже применяется, чем композиция</li>
  </ul>
</details>

<details>
  <summary>Как в React реализовать двустороннее связывание данных?</summary>
  <ul>
    <li>Через controlled components</li>
    <li>Значение элемента хранится в state, обновляется через <code>onChange</code></li>
    <li>Пример: <code>&lt;input value=&#123;state&#125; onChange=&#123;e =&gt; setState(e.target.value)&#125; /&gt;</code></li>
  </ul>
</details>

<details>
  <summary>Разница между классовым и функциональным компонентами?</summary>
  <ul>
    <li>Классовые: используют ES6-классы, методы жизненного цикла</li>
    <li>Функциональные: простые функции, используют хуки</li>
    <li>Функциональные предпочтительнее в современном React</li>
  </ul>
</details>

<details>
  <summary>Разница между useEffect() и componentDidMount()?</summary>
  <ul>
    <li><code>componentDidMount</code> вызывается один раз после монтирования (в классах)</li>
    <li><code>useEffect</code> может вызываться после каждого рендера или один раз (с <code>[]</code>)</li>
    <li><code>useEffect</code> объединяет <code>componentDidMount</code>, <code>componentDidUpdate</code>, <code>componentWillUnmount</code></li>
  </ul>
</details>

<details>
  <summary>Преимущества хуков?</summary>
  <ul>
    <li>Позволяют использовать state и жизненный цикл в функциональных компонентах</li>
    <li>Упрощают повторное использование логики (кастомные хуки)</li>
    <li>Требуют меньше кода по сравнению с классами</li>
    <li>Обеспечивают более чистую и понятную структуру компонентов</li>
  </ul>
</details>

<details>
  <summary>Недостатки хуков?</summary>
  <ul>
    <li>Сложности с оптимизацией при использовании <code>useEffect</code></li>
    <li>Запутанные зависимости в эффектах</li>
    <li>Более высокий порог входа для новичков</li>
    <li>Возможность ошибок из-за неправильного порядка вызова хуков</li>
  </ul>
</details>

<details>
  <summary>Правила (ограничения) использования хуков?</summary>
  <ul>
    <li>Хуки вызываются только на верхнем уровне функции</li>
    <li>Нельзя вызывать хуки в циклах, условиях или вложенных функциях</li>
    <li>Хуки можно использовать только в функциональных компонентах и кастомных хуках</li>
  </ul>
</details>

<details>
  <summary>Что такое поднятие состояния вверх (Lifting State Up)?</summary>
  <ul>
    <li>Техника передачи состояния в общий родительский компонент</li>
    <li>Используется для синхронизации данных между компонентами</li>
    <li>Реализация: хранить state выше по дереву и передавать через props</li>
  </ul>
</details>

<details>
  <summary>Что делает метод shouldComponentUpdate?</summary>
  <ul>
    <li>Метод классового компонента для оптимизации рендера</li>
    <li>Возвращает true/false, указывая, нужно ли перерисовывать компонент</li>
    <li>Используется для предотвращения лишних обновлений</li>
  </ul>
</details>

<details>
  <summary>Разница между createElement() и cloneElement()?</summary>
  <ul>
    <li><code>createElement</code>: создаёт новый React-элемент</li>
    <li><code>cloneElement</code>: клонирует существующий элемент и может изменять его props</li>
    <li><code>cloneElement</code> удобно использовать для передачи дополнительных пропсов детям</li>
  </ul>
</details>

<details>
  <summary>Что такое useReducer()?</summary>
  <ul>
    <li>Хук для управления состоянием через редюсер</li>
    <li>Альтернатива <code>useState</code> для сложной логики</li>
    <li>Возвращает <code>[state, dispatch]</code></li>
    <li>Подходит для предсказуемого управления состоянием</li>
  </ul>
</details>

<details>
  <summary>Как реализовать однократное выполнение операции при начальном рендеринге?</summary>
  <ul>
    <li>Использовать <code>useEffect</code> с пустым массивом зависимостей <code>[]</code></li>
    <li>Аналог <code>componentDidMount</code> в классах</li>
    <li>Пример: <code>useEffect(() =&gt; &#123; fetchData(); &#125;, [])</code></li>
  </ul>
</details>

<details>
  <summary>Что такое распределенный компонент?</summary>
  <ul>
    <li>Компонент, который предоставляет гибкий API для кастомизации через <code>children</code></li>
    <li>Позволяет разделять логику и представление</li>
    <li>Пример: Compound Components (Accordion, Tabs)</li>
  </ul>
</details>

<details>
  <summary>Расскажите о хуках useCallback(), useMemo(), useImperativeHandle(), useLayoutEffect()?</summary>
  <ul>
    <li><code>useCallback</code>: мемоизация функций, предотвращает их пересоздание</li>
    <li><code>useMemo</code>: мемоизация вычислений, возвращает кэшированное значение</li>
    <li><code>useImperativeHandle</code>: кастомизация значения, доступного через ref</li>
    <li><code>useLayoutEffect</code>: срабатывает синхронно после рендера (до отображения на экране)</li>
  </ul>
</details>

<details>
  <summary>Как отрендерить HTML код в React-компоненте?</summary>
  <ul>
    <li>Использовать <code>dangerouslySetInnerHTML</code></li>
    <li>Пример: <code>&lt;div dangerouslySetInnerHTML=&#123;&#123; __html: htmlString &#125;&#125; /&gt;</code></li>
    <li>Опасно для XSS &rarr; нужно очищать HTML</li>
  </ul>
</details>

<details>
  <summary>Зачем в setState() нужно передавать функцию?</summary>
  <ul>
    <li><code>setState</code> может работать асинхронно</li>
    <li>Функция позволяет получить актуальное предыдущее состояние</li>
    <li>Пример: <code>setState(prev =&gt; prev + 1)</code></li>
  </ul>
</details>

<details>
  <summary>Для чего предназначен метод registerServiceWorker() в React?</summary>
  <ul>
    <li>Регистрация сервис-воркера для PWA</li>
    <li>Позволяет работать офлайн, кэшировать ресурсы</li>
    <li>Используется в create-react-app (старых версиях)</li>
  </ul>
</details>

<details>
  <summary>Чем React Router отличается от обычной маршрутизации?</summary>
  <ul>
    <li>React Router — клиентская маршрутизация без перезагрузки страницы</li>
    <li>Обычная маршрутизация = запрос на сервер, полная перезагрузка</li>
    <li>React Router использует history API и SPA-подход</li>
  </ul>
</details>

<details>
  <summary>Какие хуки были добавлены в React Router версии 5?</summary>
  <ul>
    <li><code>useHistory</code> (управление историей)</li>
    <li><code>useParams</code> (доступ к параметрам маршрута)</li>
    <li><code>useLocation</code> (информация о текущем URL)</li>
    <li><code>useRouteMatch</code> (сопоставление маршрутов)</li>
  </ul>
</details>

<details>
  <summary>Как передавать пропсы в React Router?</summary>
  <ul>
    <li>Через <code>render</code> или <code>element</code></li>
    <li>Пример: <code>&lt;Route path="/profile" element=&#123;&lt;Profile user=&#123;user&#125; /&gt;&#125; /&gt;</code></li>
    <li>Также можно использовать <code>useParams</code>, <code>useLocation</code></li>
  </ul>
</details>

<details>
  <summary>Что такое Reselect и как он работает?</summary>
  <ul>
    <li>Библиотека для мемоизации селекторов в Redux</li>
    <li>Избегает лишних вычислений и ререндеров</li>
    <li>Работает по принципу: если входные данные не изменились &rarr; вернуть кэшированный результат</li>
  </ul>
</details>

<details>
  <summary>Назовите основную цель React Fiber?</summary>
  <ul>
    <li>Асинхронный рендеринг</li>
    <li>Возможность приоритезации задач</li>
    <li>Разделение обновлений на части для лучшего UX</li>
  </ul>
</details>

<details>
  <summary>Какие типы данных может возвращать render?</summary>
  <ul>
    <li>React-элементы</li>
    <li>Массивы и фрагменты</li>
    <li>Строки и числа</li>
    <li><code>null</code> и <code>boolean</code> (ничего не рендерят)</li>
  </ul>
</details>

<details>
  <summary>Разница между memo и useMemo?</summary>
  <ul>
    <li><code>React.memo</code>: мемоизация компонента (чтобы не ререндерился без изменений props)</li>
    <li><code>useMemo</code>: мемоизация вычислений внутри компонента</li>
    <li><code>memo</code> = для компонентов, <code>useMemo</code> = для значений</li>
  </ul>
</details>

<details>
  <summary>Что такое синтетические события (SyntheticEvent) в React?</summary>
  <ul>
    <li>Обёртка над нативными событиями браузера</li>
    <li>Кросс-браузерная совместимость</li>
    <li>Используются в системе событий React</li>
  </ul>
</details>

<details>
  <summary>Является ли React реактивным?</summary>
  <ul>
    <li>Нет, React декларативен, но не реактивен как, например, Vue</li>
    <li>Обновления происходят при изменении состояния, а не автоматически при изменении данных</li>
  </ul>
</details>

<details>
  <summary>Техники оптимизации перфоманса React?</summary>
  <ul>
    <li><code>React.memo</code>, <code>useMemo</code>, <code>useCallback</code></li>
    <li>Code-splitting (<code>React.lazy</code>, <code>Suspense</code>)</li>
    <li>Оптимизация рендеринга списков (key)</li>
    <li><code>shouldComponentUpdate</code> / <code>PureComponent</code></li>
    <li>Виртуализация списков (<code>react-window</code>, <code>react-virtualized</code>)</li>
  </ul>
</details>

<details>
  <summary>Лучшие практики безопасности в React?</summary>
  <ul>
    <li>Избегать <code>dangerouslySetInnerHTML</code> (или очищать HTML)</li>
    <li>Использовать Content Security Policy (CSP)</li>
    <li>Не хранить секреты в коде</li>
    <li>Проверять входные данные (валидация форм)</li>
  </ul>
</details>

<details>
  <summary>Как работает пропс children в React?</summary>
  <ul>
    <li>Специальный пропс для передачи вложенного содержимого</li>
    <li>Позволяет создавать контейнерные компоненты</li>
    <li>Пример: <code>&lt;Modal&gt;&lt;p&gt;Text&lt;/p&gt;&lt;/Modal&gt;</code></li>
  </ul>
</details>

<details>
  <summary>Что такое обратный поток данных в React?</summary>
  <ul>
    <li>Когда дочерний компонент обновляет состояние родителя</li>
    <li>Реализуется через callback-функции, передаваемые в props</li>
    <li>Пример: <code>&lt;Child onChange=&#123;setParentState&#125; /&gt;</code></li>
  </ul>
</details>

<details>
  <summary>Как использовать React.lazy и React.Suspense для запуска кода приложения?</summary>
  <ul>
    <li><code>React.lazy</code>: динамический импорт компонентов</li>
    <li><code>Suspense</code>: показывает fallback пока компонент загружается</li>
    <li>Пример:
      <pre><code class="language-jsx">
const LazyComp = React.lazy(() =&gt; import('./Comp'));
&lt;Suspense fallback=&#123;&lt;div&gt;Loading...&lt;/div&gt;&#125;&gt;
  &lt;LazyComp /&gt;
&lt;/Suspense&gt;
      </code></pre>
    </li>
  </ul>
</details>

<details>
  <summary>Что такое "Hydration" в контексте серверного-рендеренга React-приложений?</summary>
  <ul>
    <li>Hydration — процесс «оживления» HTML, сгенерированного на сервере</li>
    <li>React связывает уже готовую разметку с JavaScript</li>
    <li>Используется <code>ReactDOM.hydrate()</code></li>
  </ul>
</details>

<details>
  <summary>Разница между контролируемым и неконтролируемым компонентами в React?</summary>
  <ul>
    <li><strong>Controlled</strong>: состояние управляется через React state (<code>value</code> + <code>onChange</code>)</li>
    <li><strong>Uncontrolled</strong>: состояние хранится в DOM (доступ через ref)</li>
    <li>Controlled удобнее для сложных форм, Uncontrolled проще для быстрых решений</li>
  </ul>
</details>

