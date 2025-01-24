# DOM-and-# README: Понимание DOM и BOM в JavaScript

![image](https://github.com/user-attachments/assets/7d3a8232-5602-4dc6-bb38-de2e428fc26f)

## Введение
При работе с JavaScript в веб-разработке вы столкнетесь с двумя важными концепциями: **Document Object Model (DOM)** и **Browser Object Model (BOM)**. Этот README-файл предоставляет обзор того, что это такое, их различия и основные методы, связанные с каждым из них.

---

![image](https://github.com/user-attachments/assets/a8c86777-cd8e-4b4e-bff7-6c0563d0e72f)

## Что такое DOM?
**Document Object Model (DOM)** — это программный интерфейс для HTML- и XML-документов. Он представляет структуру документа в виде дерева объектов, где каждый узел — это объект, представляющий часть документа (например, элементы, атрибуты или текст).

### Основные особенности:
- Представляет содержимое веб-страницы.
- Позволяет динамически изменять структуру, стиль и содержимое с помощью JavaScript.

### Основные методы:
Ниже приведены наиболее часто используемые методы DOM:


![image](https://github.com/user-attachments/assets/b36ba42b-17a1-4267-af09-bf27b032d4ee)


```javascript
// Доступ к элементам
let elementById = document.getElementById('id');
let elementBySelector = document.querySelector('selector'); 
let elementsBySelector = document.querySelectorAll('selector'); 

// Манипуляция элементами
let htmlContent = elementById.innerHTML;
let textContent = elementById.textContent; 
elementById.setAttribute('attribute', 'value');
elementById.removeAttribute('attribute'); 

// Работа с событиями
elementById.addEventListener('click', () => { console.log('Clicked!'); });

// Навигация по DOM-дереву
let parent = elementById.parentNode; 
let children = elementById.childNodes; 
let firstChild = elementById.firstChild; 
let nextSibling = elementById.nextSibling;
```

![image](https://github.com/user-attachments/assets/1f3f59a4-8a59-4255-aeb9-28203ac68f06)

---

![image](https://github.com/user-attachments/assets/55fcc300-b7a0-41c5-865a-1c9f7791a78f)

## Что такое BOM?
**Browser Object Model (BOM)** представляет окружение браузера и предоставляет методы и свойства для взаимодействия с самим браузером (за пределами содержимого веб-страницы).

### Основные особенности:
- Включает такие объекты, как `window`, `navigator`, `location`, `screen` и `history`.
- Позволяет взаимодействовать с оконной средой браузера и его компонентами.

### Основные объекты и методы:
Ниже приведены ключевые объекты BOM и связанные с ними методы:

```javascript
// Объект window
window.alert('Сообщение'); 
let userConfirmed = window.confirm('Вы уверены?');
let userInput = window.prompt('Введите что-нибудь');
window.open('https://example.com', '_blank');
window.close(); // Закрыть текущее окно

// Объект navigator
console.log(navigator.userAgent);
console.log(navigator.platform);

// Объект location
console.log(location.href);
location.reload(); 
location.assign('https://example.com'); 

// Объект history
history.back(); 
history.forward(); 
history.go(-1); 

// Объект screen
console.log(screen.width); 
console.log(screen.height); 
console.log(screen.availWidth); 
console.log(screen.availHeight);
```

---

![image](https://github.com/user-attachments/assets/17d53d82-8a40-49d7-ab37-75da2f155179)

## Сравнение DOM и BOM
| Особенность         | DOM                                  | BOM                                  |
|---------------------|--------------------------------------|--------------------------------------|
| Область действия    | Содержимое и структура веб-страницы | Окружение и функции браузера         |
| Ключевой объект     | `document`                          | `window`                             |
| Назначение          | Управление HTML и CSS               | Взаимодействие с функционалом браузера |
| Примеры             | `getElementById`, `querySelector`   | `console.log`, `location.href` |

---

![image](https://github.com/user-attachments/assets/55e0031b-d96f-411c-908e-698c3993d696)

## Заключение
Понимание DOM и BOM является важным навыком для эффективного программирования на JavaScript в веб-разработке. В то время как DOM позволяет изменять содержимое страницы, BOM предоставляет возможность взаимодействовать с окружением браузера. Освоив их методы, вы сможете создавать динамичные и интерактивные веб-приложения.

---

