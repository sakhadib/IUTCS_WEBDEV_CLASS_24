### HTML Structure and Bootstrap Integration

#### Document Type and HTML Language

```html
<!DOCTYPE html>
<html lang="en">
```

- **`<!DOCTYPE html>`**: Declares the document as an HTML5 document.
- **`<html lang="en">`**: Sets the language of the document to English.

#### Head Section

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adib Sakhawat</title>

    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="..." crossorigin="anonymous">
    <script defer src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="..." crossorigin="anonymous"></script>

    <link rel="stylesheet" href="profile.css">
</head>
```

- **Meta Tags**:
  - `<meta charset="UTF-8">`: Sets character encoding to UTF-8.
  - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Ensures proper rendering on mobile devices.

- **Title**:
  - `<title>Adib Sakhawat</title>`: Sets the title of the webpage.

- **Bootstrap CSS Integration**:
  - `<link href="...bootstrap.min.css" rel="stylesheet" ...>`: Links the Bootstrap CSS from a CDN.
  - **Bootstrap Classes Available**: All Bootstrap CSS classes, such as grid system, typography, buttons, tables, etc.

- **Bootstrap JS Integration**:
  - `<script defer src="...bootstrap.bundle.min.js" ...></script>`: Includes Bootstrap's JavaScript bundle for interactive components.
  - **Bootstrap Components Enabled**: Modals, dropdowns, carousels, etc.

- **Custom CSS**:
  - `<link rel="stylesheet" href="profile.css">`: Links to the custom CSS file for additional styling.

#### Body Section

```html
<body>
    <header>
        <!-- Empty header; can be used for navigation or branding -->
    </header>

    <main>
        <!-- Main content goes here -->
    </main>
</body>
```

- **`<header>`**: Currently empty but reserved for future content like navigation menus.
- **`<main>`**: Contains the main content of the page.

---

### Main Content Structure

#### Container

```html
<div class="container">
    <!-- Content inside the container -->
</div>
```

- **Bootstrap Class**: `container`
  - Centers the content and provides horizontal padding.
  - Ensures the content is responsive and adjusts according to screen size.

#### Hero Section

```html
<div class="row hero">
    <!-- Hero section content -->
</div>
```

- **Bootstrap Class**: `row`
  - Creates a horizontal group of columns.
- **Custom Class**: `hero`
  - Applies custom styles defined in `profile.css` for vertical centering and minimum height.

##### Image Column

```html
<div class="col-md-4 image-container">
    <img src="harry.png" alt="" class="profile_pic">
</div>
```

- **Bootstrap Class**: `col-md-4`
  - Defines a column that takes up 4 out of 12 grid columns on medium to large screens.
- **Custom Class**: `image-container`
  - Centers the image within the column.
- **Image Element**:
  - `<img src="harry.png" alt="" class="profile_pic">`
    - **Custom Class**: `profile_pic`
      - Styles the image to have specific dimensions and a circular shape.

##### Text Column

```html
<div class="col-md-8">
    <h1 class="display-6">Harry James Potter</h1>
    <h1 class="fs-4">Wizard</h1>

    <p class="lead description">
        <!-- Description text -->
    </p>

    <a href="https://en.wikipedia.org/wiki/Harry_Potter" target="_blank" class="btn btn-dark">Learn More</a>
</div>
```

- **Bootstrap Class**: `col-md-8`
  - Occupies the remaining 8 grid columns on medium to large screens.
- **Heading Elements**:
  - `<h1 class="display-6">`: Uses Bootstrap's `display-6` class for large headings.
  - `<h1 class="fs-4">`: Uses `fs-4` to set the font size to 1.5rem.
- **Paragraph Element**:
  - `<p class="lead description">`: Combines Bootstrap's `lead` class for emphasis and a custom `description` class for text alignment.
- **Button Element**:
  - `<a href="..." class="btn btn-dark">`: Uses Bootstrap's button classes to style the link as a dark button.

---

### Additional Information Sections

#### Section Headers

```html
<div class="row">
    <div class="col-md-6">
        <h1 class="display-6">
            Personal Information
        </h1>
    </div>
    <div class="col-md-6">
        <h1 class="display-6">
            Educational Information
        </h1>
    </div>
</div>
```

- **Bootstrap Classes**:
  - `row`: Creates a horizontal group of columns.
  - `col-md-6`: Each column occupies half the width on medium to large screens.
- **Heading Elements**:
  - `<h1 class="display-6">`: Uses Bootstrap's `display-6` for section titles.

#### Information Tables

```html
<div class="row">
    <!-- Personal Information Table -->
    <div class="col-md-5 mt-4">
        <table class="table">
            <!-- Table content -->
        </table>
    </div>

    <!-- Educational Information Table -->
    <div class="col-md-5 offset-md-1 mt-4">
        <table class="table">
            <!-- Table content -->
        </table>
    </div>
</div>
```

- **Bootstrap Classes**:
  - `col-md-5`: Each table column occupies 5 grid columns.
  - `offset-md-1`: Adds a left margin equivalent to 1 grid column to the second table for spacing.
  - `mt-4`: Adds a top margin to the tables.
  - `table`: Styles the table with Bootstrap's default table styles.

##### Table Content

- **Table Structure**:

```html
<table class="table">
    <tbody>
        <tr>
            <th scope="row">First Name</th>
            <td>Harry</td>
        </tr>
        <!-- Additional rows -->
    </tbody>
</table>
```

- **Bootstrap Classes**:
  - `table`: Applies Bootstrap's table styling.
  - **Table Elements**:
    - `<tr>`: Table row.
    - `<th scope="row">`: Header cell for row labels.
    - `<td>`: Standard data cell.

---

### Custom CSS Explained (`profile.css`)

#### Hero Section Styling

```css
.hero {
    min-height: 50vh;
    display: flex;
    align-items: center;
}
```

- **`.hero` Class**:
  - `min-height: 50vh;`: Ensures the hero section takes up at least half the viewport height.
  - `display: flex;`: Enables Flexbox layout for flexible positioning.
  - `align-items: center;`: Vertically centers the content within the hero section.

#### Image Container Styling

```css
.image-container {
    display: flex;
    justify-content: center;
}
```

- **`.image-container` Class**:
  - `display: flex;`: Uses Flexbox to align items.
  - `justify-content: center;`: Horizontally centers the image within the container.

#### Profile Picture Styling

```css
.profile_pic {
    width: 300px;
    height: 300px;
    border-radius: 50%;
}
```

- **`.profile_pic` Class**:
  - `width: 300px;`: Sets a fixed width for the image.
  - `height: 300px;`: Sets a fixed height for the image.
  - `border-radius: 50%;`: Makes the image circular by rounding the corners.

#### Description Text Styling

```css
.description {
    text-align: justify;
}
```

- **`.description` Class**:
  - `text-align: justify;`: Aligns the text to both the left and right margins, adding extra space between words as necessary.

---

### How the Page Works

- **Responsive Design**:
  - Utilizes Bootstrap's grid system (`container`, `row`, `col-*` classes) to create a responsive layout that adjusts to different screen sizes.
  - Columns stack vertically on smaller screens and align horizontally on medium to large screens.

- **Typography and Styling**:
  - Bootstrap classes like `display-6`, `fs-4`, and `lead` are used for consistent typography and to emphasize important text.
  - Custom CSS classes add specific styles not covered by Bootstrap, such as the circular profile picture and justified text.

- **Layout and Alignment**:
  - Flexbox is used in custom CSS (`display: flex;`) to vertically and horizontally center content within sections.
  - Margins (`mt-4`) and offsets (`offset-md-1`) from Bootstrap are used to space out elements appropriately.

- **Interactive Elements**:
  - The "Learn More" button uses Bootstrap's button classes (`btn`, `btn-dark`) to create a styled button that links to an external page.
  - The `target="_blank"` attribute opens the link in a new tab.

---

### Bootstrap vs. Custom Classes

#### Bootstrap Classes

- **Layout and Grid System**:
  - `container`, `row`, `col-md-*`, `offset-md-*`: For structuring the page layout responsively.
- **Typography**:
  - `display-6`: Large display headings.
  - `fs-4`: Font size utility class for headings.
  - `lead`: Emphasized paragraph text.
- **Spacing Utilities**:
  - `mt-4`: Adds a top margin (`margin-top`) to elements.
- **Buttons**:
  - `btn`, `btn-dark`: Styles links as buttons with a dark background.
- **Tables**:
  - `table`: Applies Bootstrap's table styling for consistent look and feel.

#### Custom Classes

- **`.hero`**:
  - Styles the hero section for vertical centering and minimum height.
- **`.image-container`**:
  - Centers the profile image within its column.
- **`.profile_pic`**:
  - Styles the profile image to be circular and sets its dimensions.
- **`.description`**:
  - Justifies the text within the description paragraph for better readability.

---

### Summary

The webpage effectively combines Bootstrap's powerful grid system and components with custom CSS to create a responsive and visually appealing profile page. Bootstrap classes handle the majority of the layout, typography, and component styling, ensuring consistency and responsiveness across devices. Custom classes are used to fine-tune the appearance, such as centering elements and applying unique styles not provided by Bootstrap.

By leveraging both Bootstrap and custom CSS, the page maintains a balance between utilizing a robust framework and achieving a unique design tailored to the content.
