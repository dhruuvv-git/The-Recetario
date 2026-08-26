# The Recetario 📖

![Release](https://img.shields.io/badge/release-v1.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Android-lightgrey.svg)
![Tech](https://img.shields.io/badge/built%20with-Electron%20%7C%20Capacitor-brightgreen.svg)

The Recetario is a cross-platform digital heirloom cookbook that combines rustic journal aesthetics with macro and nutrition tracking. Built with Electron for desktop and Capacitor for android, it presents recipes inside an interactive 3D book spread complete with custom ingredient databases, bookmark tab filters, and full export/import capabilities across platforms.

---

## Key Features

* **Interactive 3D Book Experience:** Flip through a digital notebook complete with realistic page-turning animations, polaroid-style dish cards, margin bookmark ribbons, and handwritten note styling.
* **Granular Macro Tracking:** Automatically calculates total calories, protein, carbohydrates, and fat based on ingredient weights (g). Includes raw vs. cooked ingredient variants for accurate nutritional totals.
* **Custom Ingredient Database:** Search through an extensive pre-built ingredient library or add custom ingredients with macros per 100g, persisted locally on device storage.
* **Smart Categorization & Search:** Filter by meal type (*Breakfast, Lunch, Dinner, Dessert, Snack*), custom tagged categories with outline icons, or mark dishes as favorites.
* **Seamless Export & Import:**
  * **JSON Backup:** Save and restore complete recipe databases.
  * **PDF Export & Ingestion:** Generates single/multi-page recipe PDFs with embedded metadata (`RecetarioData<<<...>>>`), allowing full database restoration directly from exported PDF files via PDF.js.

---

## Downloads & Releases

Check out the [Releases Page](https://github.com/YOUR_USERNAME/YOUR_REPO/releases) to download the latest stable pre-built packages.

| Version | File | Target Platform | Description |
| :--- | :--- | :--- | :--- |
| `v1.0` | `The-Recetario-v1.0-Setup.exe` | Windows PC | Desktop standalone application built with Electron. |
| `v1.0` | `The-Recetario-v1.0.apk` | Android | Mobile standalone package built with Capacitor. |

---

## Tech Stack

| Layer | Technology / Library |
| :--- | :--- |
| **Desktop Runtime** | Electron (Windows `.exe`) |
| **Mobile Runtime** | Capacitor (Android `.apk`) |
| **Frontend Framework** | HTML5, CSS3 (3D Transforms, CSS Variables), Modern JavaScript (ES6+) |
| **Typography & Icons** | Google Fonts (*Libre Caslon Text, Work Sans, Caveat*), Material Symbols |
| **PDF Generation** | `jspdf`, `html2canvas` |
| **PDF Parsing** | `pdf.js` |
| **Storage** | Device Local Storage / Native File System |

---

## Nutritional Logic

Macros are dynamically computed from ingredient gram weight (g) against nutritional profiles per 100g:

$$\text{Macro Total} = \sum \left( \frac{\text{Ingredient Weight (g)} \times \text{Macro per 100g}}{100} \right)$$

Dishes are automatically tagged with nutritional profile badges (e.g., *Bulk Phase*, *Lean Cut*, *Balanced Meal*, *High Kcal*) based on calorie and protein density.

---

## Getting Started

1. Go to the [Releases](../../releases) tab and grab the latest **`v1.0`** binary for your system:
   * **Windows:** Download and run the `.exe` installer or standalone executable.
   * **Android:** Download and install the `.apk` file directly on your mobile device.
2. Launch the application.
3. Tap or click the book cover to open your personal collection and start recording recipes.
