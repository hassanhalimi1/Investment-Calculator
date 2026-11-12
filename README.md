# Investment Calculator

A sleek and interactive Investment Calculator built with React 19 and Vite. Estimate the future value of your investments by adjusting your initial capital, annual contributions, expected annual return, and investment duration.

The application calculates and displays year-by-year investment projections, including accumulated interest, total interest earned, and invested capital.

## ✨ Features

- Initial Investment: Set your starting investment amount.
- Annual Contributions: Define how much you plan to invest each year.
- Expected Return: Enter your expected annual rate of return.
- Investment Duration: Choose the number of years for your investment plan.
- Automatic Calculations: Instantly recalculate projections whenever input values change.
- Year-by-Year Breakdown: View investment performance for every year.
- Interest Tracking: See annual interest and cumulative interest earned.
- Invested Capital Tracking: Monitor the total capital contributed over time.
- Currency Formatting: Displays financial results in USD using the JavaScript Internationalization API.
- Interactive Interface: Simple input controls and a clean, responsive visual design.

## 🛠️ Tech Stack

| Technology        | Purpose                                       |
| ----------------- | --------------------------------------------- |
| React 19          | Building the user interface                   |
| Vite              | Development server and build tooling          |
| JavaScript (ES6+) | Investment calculations and application logic |
| CSS3              | Styling and layout                            |
| HTML5             | Application structure                         |
| Intl API          | Currency formatting                           |

## 🚀 Getting Started

Follow these instructions to run the project locally.

### Prerequisites

Make sure you have installed:

- [Node.js](https://nodejs.org/?utm_source=chatgpt.com)
- npm (included with Node.js)

### Installation

1\. Clone the repository

```
git clone <your-repository-url>
```

2\. Navigate to the project directory

```
cd <project-directory>
```

3\. Install dependencies

```
npm install
```

4\. Start the development server

```
npm run dev
```

5\. Open the application

Visit the local URL displayed in your terminal, usually:

```
http://localhost:5173
```

## 💡 How to Use

The calculator requires four inputs:

| Input              | Description                                    |
| ------------------ | ---------------------------------------------- |
| Initial Investment | The amount of money invested at the beginning. |
| Annual Investment  | The additional amount invested each year.      |
| Expected Return    | The expected annual percentage return.         |
| Duration           | The investment period in years.                |

Once the values are entered, the application automatically calculates and displays the projected investment results.

## 📊 Understanding the Results

The results table provides a financial breakdown for each investment year.

| Column           | Description                                                  |
| ---------------- | ------------------------------------------------------------ |
| Year             | The investment year.                                         |
| Investment Value | Total projected investment value at the end of the year.     |
| Interest (Year)  | Interest earned during that particular year.                 |
| Total Interest   | Cumulative interest earned since the beginning.              |
| Invested Capital | Total capital contributed, including the initial investment. |

## 🧮 Calculation Logic

The investment calculation is implemented in `src/util/investment.js`.

The application calculates annual interest using the following formula:

\\[ \text{Annual Interest} = \text{Investment Value} \times \frac{\text{Expected Return}}{100} \\]

The investment value is then updated:

\\[ \text{New Investment Value} = \text{Previous Value} + \text{Annual Interest} + \text{Annual Investment} \\]

This process repeats for the selected investment duration.

Note: These calculations are projections based on a constant annual return. Actual investment performance may differ, and the calculator does not account for taxes, fees, inflation, or market fluctuations.

## 📂 Project Structure

```
.
├── public/
│   └── investment-calculator-logo.png
│
├── src/
│   ├── assets/
│   │   └── investment-calculator-logo.png
│   │
│   ├── components/
│   │   ├── Header.jsx
│   │   ├── Results.jsx
│   │   └── UserInput.jsx
│   │
│   ├── util/
│   │   └── investment.js
│   │
│   ├── App.jsx
│   ├── index.css
│   └── index.jsx
│
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

## ⚙️ Available Scripts

The following commands are available through npm:

| Command           | Description                            |
| ----------------- | -------------------------------------- |
| `npm run dev`     | Starts the local development server.   |
| `npm run build`   | Builds the application for production. |
| `npm run preview` | Previews the production build locally. |
| `npm run lint`    | Runs ESLint to check code quality.     |

## 🏗️ Building for Production

Generate an optimized production build:

```
npm run build
```

The generated files will be available inside the `dist/` directory.

To preview the production build locally:

```
npm run preview
```

## 🧠 Implementation Details

- State Management: React's `useState` hook manages the investment input values.
- Controlled Inputs: Input components synchronize user-entered values with application state.
- Dynamic Calculations: Investment projections are recalculated whenever the input values change.
- Reusable Components: The application separates the header, input controls, and results table into individual components.
- Financial Formatting: `Intl.NumberFormat` formats numerical results as US dollars.
- Input Validation: The application checks that the investment duration is greater than zero before displaying results.

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome!

1. Fork this repository.
2. Create a feature branch:
   ```
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```
   git commit -m "Add: your feature"
   ```
4. Push your branch:
   ```
   git push origin feature/your-feature
   ```
5. Open a Pull Request describing your improvements.
