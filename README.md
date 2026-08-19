# The Recetario 📖

**The Recetario** is a web-based digital heirloom cookbook that combines rustic journal aesthetics with macro and nutrition tracking. Built with vanilla HTML, CSS, and JavaScript, it presents recipes inside an interactive 3D book spread complete with custom ingredient databases, bookmark tab filters, and full export/import capabilities.

---

## Key Features

* **Interactive 3D Book Experience:** Flip through a digital notebook complete with realistic page-turning animations, polaroid-style dish cards, margin bookmark ribbons, and handwritten note styling.
* **Granular Macro Tracking:** Automatically calculates total calories, protein, carbohydrates, and fat based on ingredient weights (g). Includes raw vs. cooked ingredient variants for accurate nutritional totals.
* **Custom Ingredient Database:** Search through an extensive pre-built ingredient library or add custom ingredients with macros per 100g, persisted locally in `localStorage`.
* **Smart Categorization & Search:** Filter by meal type (Breakfast, Lunch, Dinner, Dessert, Snack), custom tagged categories with outline icons, or mark dishes as favorites.
* **Seamless Export & Import:**
  * **JSON Backup:** Save and restore complete recipe databases.
  * **PDF Export & Ingestion:** Generates single/multi-page recipe PDFs with embedded metadata (`RecetarioData<<<...>>>`), allowing full database restoration directly from exported PDF files via PDF.js.

---

## Tech Stack

| Layer | Technology / Library |
| :--- | :--- |
| **Frontend Framework** | Vanilla HTML5, CSS3 (3D Transforms, CSS Variables), Modern JavaScript (ES6+) |
| **Typography & Icons** | Google Fonts (*Libre Caslon Text*, *Work Sans*, *Caveat*), Material Symbols |
| **PDF Generation** | `jspdf`, `html2canvas` |
| **PDF Parsing** | `pdf.js` |
| **Storage** | Browser `localStorage` |

---

## Nutritional Logic

Macros are dynamically computed from ingredient gram weight (g) against nutritional profiles per 100g:

$$\text{Macro Total} = \sum \left( \text{Ingredient Weight (g)} \times \frac{\text{Macro per 100g}}{100} \right)$$

Dishes are automatically tagged with nutritional profile badges (e.g., *Bulk Phase*, *Lean Cut*, *Balanced Meal*, *High Kcal*) based on calorie and protein density.

---

## Getting Started

1. Clone or download the repository.
2. Open `index.html` directly in any standard modern web browser—no local server or build step required.
3. Tap the book cover to open your personal collection and start recording recipes.
