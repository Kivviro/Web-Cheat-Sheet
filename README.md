# 🎨 CSS Cheat Sheet

[Полное руководство](https://developer.mozilla.org/ru/docs/Web/CSS/Reference)

## 1. Что такое CSS

**CSS (Cascading Style Sheets)** — это язык стилей, используемый для описания внешнего вида элементов HTML-документа. С его помощью можно задавать цвета, шрифты, отступы, расположение элементов и многое другое.

---

## 2. Способы подключения стилей на страницу

### 2.1 Встроенный (inline)

```html
<p style="color: green; font-size: 18px;">Текст с встроенным стилем</p>
```

### 2.2 Внутренний (в теге `<style>` внутри `<head>`)

```html
<head>
  <style>
    p {
      color: red;
    }
  </style>
</head>
```

### 2.3 Внешний (в отдельном `.css` файле)

**HTML (index.html):**
```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

**CSS (styles.css):**
```css
p {
  color: blue;
}
```

---

## 3. Основные теги и единицы измерения

### Полезные HTML теги в контексте CSS:

| Тег       | Назначение                      | Пример                        |
|-----------|----------------------------------|-------------------------------|
| `<div>`   | Контейнер, блочный элемент       | `<div class="box"></div>`     |
| `<span>`  | Контейнер, строчный элемент      | `<span style="color:red">Текст</span>` |
| `<p>`     | Абзац                            | `<p>Пример текста</p>`        |
| `<h1>`-`<h6>` | Заголовки уровней             | `<h1>Заголовок</h1>`          |
| `<a>`     | Ссылка                           | `<a href="#">Ссылка</a>`      |
| `<img>`   | Изображение                      | `<img src="image.jpg">`       |
| `<ul>` `<li>` | Списки                        | `<ul><li>Элемент</li></ul>`   |

---

### 4.1 Единицы измерения:

- `px` — пиксели. Абсолютная единица измерения.
- `em` — относительная единица, зависит от размера шрифта родителя.
- `rem` — относительная единица, зависит от размера шрифта корневого (`html`).

**Пример:**
```css
body {
  font-size: 16px;
}
h1 {
  font-size: 2em;  /* = 32px */
}
p {
  font-size: 1rem; /* = 16px */
}
```

---

## 5. Блочная модель CSS

**CSS Box Model** описывает прямоугольную коробку, которая образует каждый элемент:

1. **Content** — Содержимое элемента (текст, изображение).
2. **Padding** — Внутренние отступы от содержимого до границы.
3. **Border** — Граница элемента.
4. **Margin** — Внешний отступ от других элементов.

**Пример:**

```css
.box {
  width: 200px;
  height: 100px;
  padding: 10px;
  border: 5px solid black;
  margin: 20px;
}
```

**Иллюстрация:**
```
+---------------------------+
|        Margin             |
|  +---------------------+  |
|  |      Border         |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  | +-----------+ |  |  |
|  |  | |  Content  | |  |  |
|  |  | +-----------+ |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

---

## 6. Пример простого красивого сайта (HTML + CSS)

**index.html**
```html
<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <title>Мой Сайт</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Добро пожаловать на мой сайт!</h1>
    <p>Это мой первый сайт на HTML и CSS.</p>
  </header>

  <section class="content">
    <h2>О сайте</h2>
    <p>Здесь будет много интересного контента.</p>
  </section>

  <footer>
    <p>&copy; 2025 Мой сайт</p>
  </footer>
</body>
</html>
```

**style.css**
```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background-color: #f4f4f4;
  color: #333;
}

header {
  background-color: #4CAF50;
  color: white;
  padding: 40px 20px;
  text-align: center;
}

.content {
  padding: 20px;
}

footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 15px 0;
  position: fixed;
  bottom: 0;
  width: 100%;
}
```

---
