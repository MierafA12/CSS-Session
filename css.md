# CSS Basics for Absolute Beginners

CSS (Cascading Style Sheets) is a language used to style HTML content. This session introduces you to the essential concepts of CSS.

---

## Table of Contents

1. **What is CSS?**
2. **Ways to Apply CSS**
3. **CSS Syntax**
4. **Selectors**
5. **Box Model**
6. **Positioning**
7. **Color and Backgrounds**
8. **Text Styling**
9. **Flexbox**
10. **Grid**
11. **Animation**
12. **Media Queries**
13. **Units of Measurement**
14. **Practice Exercise**

---

## 1. What is CSS?
CSS is a stylesheet language used to describe the presentation of an HTML document. It controls the layout, colors, fonts, and more.

### Why use CSS?
- Separate content (HTML) from design (CSS).
- Reuse styles across multiple pages.
- Enhance user experience.

---

## 2. Ways to Apply CSS
1. **Inline CSS**: Applied directly to an HTML element using the `style` attribute.
   ```html
   <p style="color: blue;">This is a blue paragraph.</p>
   ```

2. **Internal CSS**: Defined within a `<style>` tag inside the `<head>` section.
   ```html
   <style>
       p {
           color: blue;
       }
   </style>
   ```

3. **External CSS**: Written in a separate `.css` file and linked to the HTML.
   ```html
   <link rel="stylesheet" href="styles.css">
   ```

---

## 3. CSS Syntax
A CSS rule consists of a selector and a declaration block.

```css
selector {
    property: value;
}
```

### Example
```css
p {
    color: red;
    font-size: 16px;
}
```

---

## 4. Selectors
Selectors are used to target HTML elements.

### Types of Selectors
1. **Universal Selector**: Targets all elements.
   ```css
   * {
       margin: 0;
   }
   ```

2. **Type Selector**: Targets specific HTML tags.
   ```css
   h1 {
       color: green;
   }
   ```

3. **Class Selector**: Targets elements with a specific class.
   ```css
   .example {
       font-style: italic;
   }
   ```

4. **ID Selector**: Targets an element with a specific ID.
   ```css
   #unique {
       background-color: yellow;
   }
   ```

5. **Group Selector**: Targets multiple selectors.
   ```css
   h1, h2, p {
       font-family: Arial, sans-serif;
   }
   ```

---

## 5. Box Model
The box model describes how elements are displayed on the web.

### Components
- **Content**: The actual content of the box.
- **Padding**: Space between content and border.
- **Border**: The edge of the box.
- **Margin**: Space outside the border.

```css
.box {
    width: 100px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```

---

## 6. Positioning
CSS positioning specifies the placement of elements on a page.

### Types
1. **Static**: Default position.
   ```css
   div {
       position: static;
   }
   ```

2. **Relative**: Positioned relative to its normal position.
   ```css
   div {
       position: relative;
       top: 10px;
   }
   ```

3. **Absolute**: Positioned relative to the nearest positioned ancestor.
   ```css
   div {
       position: absolute;
       top: 20px;
       left: 50px;
   }
   ```

4. **Fixed**: Positioned relative to the viewport.
   ```css
   div {
       position: fixed;
       bottom: 0;
   }
   ```

5. **Sticky**: Toggles between relative and fixed based on scroll.
   ```css
   div {
       position: sticky;
       top: 0;
   }
   ```

---

## 7. Color and Backgrounds

### Colors
- Named Colors: `red`, `blue`, `green`
- Hexadecimal: `#ff0000`
- RGB: `rgb(255, 0, 0)`
- HSL: `hsl(0, 100%, 50%)`

### Backgrounds
- Background Color:
  ```css
  body {
      background-color: lightblue;
  }
  ```

- Background Image:
  ```css
  body {
      background-image: url('background.jpg');
  }
  ```

---

## 8. Text Styling

### Properties
- **Font Family**: Defines the font.
  ```css
  p {
      font-family: Arial, sans-serif;
  }
  ```

- **Font Size**: Adjusts the size of text.
  ```css
  h1 {
      font-size: 24px;
  }
  ```

- **Text Alignment**: Aligns text.
  ```css
  h1 {
      text-align: center;
  }
  ```

- **Text Decoration**: Adds decoration (underline, overline, etc.).
  ```css
  a {
      text-decoration: none;
  }
  ```

---

## 9. Flexbox
Flexbox is a layout model for aligning items in a container.

### Example
```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
```

---

## 10. Grid
Grid is a powerful layout system for creating two-dimensional designs.

### Example
```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
}

.item {
    background-color: lightgray;
    padding: 20px;
    text-align: center;
}
```

---

## 11. Animation
CSS animations allow elements to change styles smoothly over time.

### Example
```css
@keyframes slideIn {
    from {
        transform: translateX(-100%);
    }
    to {
        transform: translateX(0);
    }
}

.element {
    animation: slideIn 2s ease-in-out;
}
```

---

## 12. Media Queries
Media queries make web pages responsive by applying styles based on screen size.

### Example
```css
@media (max-width: 600px) {
    body {
        background-color: lightgray;
    }
}

@media (min-width: 601px) {
    body {
        background-color: white;
    }
}
```

---

## 13. Units of Measurement
CSS provides various units to define sizes, lengths, and spacing. These units can be broadly categorized into **absolute** and **relative** units.

### Absolute Units
- **px (pixels)**: Fixed size. Commonly used for precise control.
  ```css
  p {
      font-size: 16px;
  }
  ```

- **cm (centimeters), mm (millimeters), in (inches)**: Rarely used in web design.

### Relative Units
- **em**: Relative to the font size of the parent element.
  ```css
  p {
      font-size: 2em; /* 2 times the parent font size */
  }
  ```

- **rem (root em)**: Relative to the root element's font size.
  ```css
  p {
      font-size: 1.5rem; /* 1.5 times the root font size */
  }
  ```

- **% (percent)**: Relative to the parent element.
  ```css
  div {
      width: 50%;
  }
  ```

- **vw (viewport width) and vh (viewport height)**: Relative to the viewport.
  ```css
  div {
      height: 50vh;
}

  ```