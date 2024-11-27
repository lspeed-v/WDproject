# LSpeed's portfolio Web Design.

## **Theme Toggle Functionality**
```javascript
// Theme toggle functionality
const themeToggle = document.getElementById('themeToggle');
themeToggle.addEventListener('click', () => {
    document.body.classList.toggle('light-theme');
    themeToggle.textContent = document.body.classList.contains('light-theme') ? '☀️' : '🌙';
});
```

### **Description**
This script implements a **theme toggle** feature, allowing users to switch between a **dark theme** (default) and a **light theme**.

### **Logic**
1. **Select the Theme Toggle Button**  
   The button is identified using its `id="themeToggle"`.

2. **Event Listener for Button Click**  
   When the button is clicked:
   - It toggles the `light-theme` class on the `<body>` element.  
   - If the class exists, it switches to the **light theme**; otherwise, the **dark theme** is applied.

3. **Dynamic Button Text**  
   - If the theme is light, the button shows the `☀️` icon.  
   - If the theme is dark, the button shows the `🌙` icon.

### **Purpose**
This feature enhances **usability** by allowing users to customize the visual style of the website.

---

## **Scroll Animation for Sections**
```javascript
document.addEventListener("DOMContentLoaded", function () {
    const sections = document.querySelectorAll(".home-section");

    const handleScroll = () => {
        sections.forEach((section) => {
            const rect = section.getBoundingClientRect();
            if (rect.top >= 0 && rect.top <= window.innerHeight) {
                section.classList.add("animate");
            }
        });
    };

    // Listen for scroll events
    window.addEventListener("scroll", handleScroll);

    // Run on initial page load
    handleScroll();
});
```

### **Description**
This script applies a **scroll animation** to sections of the page, making them appear or animate as they enter the viewport.

### **Logic**
1. **Detect Sections**  
   The script selects all elements with the `.home-section` class.

2. **Scroll Event Listener**  
   It listens for the `scroll` event on the window.

3. **Animation Logic**  
   - When the page is scrolled, the script checks each section's position using the `getBoundingClientRect()` method.
   - If the section's top edge is visible within the viewport (`rect.top >= 0` and `rect.top <= window.innerHeight`), it adds the `.animate` class to that section.

4. **Initial Execution**  
   The `handleScroll` function is called when the page is loaded to immediately handle any sections that are already visible.

### **Purpose**
The purpose of this script is to enhance the user experience by adding smooth animations to sections as they come into view during scrolling.
