# 👻 Interactive Spooky Login Form

## Project Name: Interactive Spooky Login Form

A unique and engaging login form featuring an animated SVG ghost that dynamically reacts to user interactions with the input fields. The ghost's eyes follow the cursor/text input, its mouth changes expression based on the email field's validity, and its arms cover its eyes when the password field is focused.

## ✨ Key Features

* **Animated SVG Ghost:** A custom-drawn SVG ghost is embedded directly into the HTML.
    * **Floating Animation:** The entire ghost body has a subtle, continuous vertical float animation applied via CSS `@keyframes float`.
    * **Arm Float:** The ghost's arms also have a separate, staggered floating animation (`@keyframes float-arm`).
* **Interactive Eyes (Pupil Tracking):**
    * As the user types in the **Email field**, the ghost's pupils track the length of the input. The longer the email, the further the pupils move to the right (`updateMouthEyes` function).
    * On `blur` (when the user leaves the email field), the pupils snap back to their original center position.
* **Dynamic Mouth Expression:**
    * **Default:** A small, slightly sad or neutral mouth.
    * **Typing/Invalid Email:** When the email field has input but no valid `@` or the `@` is at the beginning/end, the mouth becomes slightly worried/pursed.
    * **Valid Email:** When a valid email structure is detected (contains `@` and text before/after it), the mouth opens into a wider, more satisfied or surprised expression.
* **Password Reaction (The Spooky Part):**
    * **On Password Focus:** When the user clicks into the **Password field**, the ghost's arms instantly move and cross over its eyes, as if scared or shy. This is achieved by changing the SVG `d` path attribute.
    * **On Password Blur:** When the user leaves the password field, the arms return to their normal floating position.
* **Custom Styling:** Uses the `K2D` and `Roboto` fonts with a distinct, slightly spooky color palette (using orange/brown hues) applied to the form and background.
* **Animated Placeholder:** The email field features a placeholder that animates up and shrinks when the field is focused.

## 🛠️ Technology Stack

* **HTML (`index.html`):** Defines the form structure and embeds the complete interactive **SVG ghost**.
* **CSS (`style.css`):** Handles all visual styling, layout, the spooky color theme, and the CSS `@keyframes` for the ghost's floating motion.
* **JavaScript (`script.js`):** Contains all the logic for user interaction and dynamic SVG manipulation.
    * **`updateMouthEyes()`:** The core function for pupil tracking and mouth expression changes based on email field content.
    * **Event Listeners:** Used to detect `focus`, `blur`, and `input` events on the email and password fields.

## 🚀 Getting Started

1.  **Clone the Repository:**
    ```bash
    git clone [Your Repository URL]
    ```
2.  **Open the File:**
    Open the `index.html` file directly in your web browser.

### Interaction

* **Type in Email:** Watch the ghost's pupils follow your input. Try typing a valid vs. invalid email format to see the mouth change.
* **Click Password:** Watch the ghost's arms immediately fly up to cover its eyes.

## ⚙️ SVG/JS Manipulation (From `script.js`)

| Action | JavaScript Element | Method/Property Changed |
| :--- | :--- | :--- |
| **Pupil Tracking** | `#pupil-right`, `#pupil-left` | `setAttribute("cx", ...)` and `setAttribute("cy", ...)` |
| **Mouth Expression** | `#mouth` | `setAttribute("d", ...)` (changes the SVG path data) |
| **Arm Over Eyes** | `#ghost-arm-left`, `#ghost-arm-right` | `setAttribute("d", ...)` (changes the SVG path data) |
| **Floating** | `#ghost-body`, `.ghost-arm` | CSS `@keyframes` in the SVG `<style>` tag |

## 📸 Screenshots

*(Add a screenshot or GIF of your interactive cube here)*
