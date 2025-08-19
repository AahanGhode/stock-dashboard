
# Stock Dashboard
#### Video Demo: https://www.youtube.com/watch?v=Dk_U3xasSNk

#### Description:

Stock Dashboard is a modern, interactive web application that allows users to track, visualize, and manage a personalized list of stocks in real time. Built with React, Vite, and Tailwind CSS, this project is designed for anyone interested in monitoring the stock market, learning about stock data visualization, or building a finance-related web app. The dashboard features a clean, responsive user interface, dynamic stock widgets, interactive charts, and a customizable watchlist, making it a robust tool for both casual investors and finance enthusiasts.

The main application logic resides in `App.jsx`. This file manages the global state for the stock list, the currently selected stock, and form fields for adding new stocks. It also handles local storage persistence, so your watchlist is saved between sessions. The `useEffect` hooks in `App.jsx` are used to load and save stocks, as well as to dynamically inject TradingView widgets for real-time stock data. The design choice to use local storage was made for simplicity and to avoid backend complexity, but the code is structured so that a backend API could be integrated in the future.

The `AddNewStock.jsx` component provides a form for users to add new stocks to their watchlist. It uses controlled inputs for the stock symbol, name, and sector, and includes validation to prevent empty fields or duplicate entries. The add button uses an icon from the `react-icons` library for a modern look. This component receives its state and handlers as props from `App.jsx`, following React best practices for state management.

The `StockListTable.jsx` component displays the user's stocks in a scrollable, sortable, and filterable table. It supports searching by symbol or name, sorting by name or sector, and filtering by sector. Each row includes action buttons for editing or removing a stock, with edit and delete icons for clarity. The table is designed to be responsive and user-friendly, with hover effects and clear visual cues. The table head is managed by `StockListTableHead.jsx`, which provides sorting and filtering controls.

`StockListHeader.jsx` serves as the header for the stock list section. It includes a title, a brief description, and controls for saving the stock list to a JSON file or loading a list from a file. This feature was added to make it easy for users to back up or transfer their watchlists, and to demonstrate file handling in React.

The `StockChart.jsx` component displays an interactive chart for the currently selected stock, using a TradingView widget. The chart updates automatically when the selected stock changes. The decision to use TradingView was based on its reliability, real-time data, and ease of integration. The chart is styled to match the application's dark theme and is fully responsive.

Supporting components include `Button.jsx` and `Input.jsx`, which are reusable UI elements styled with Tailwind CSS. `Button.jsx` standardizes the appearance and behavior of buttons throughout the app, while `Input.jsx` does the same for text inputs. This modular approach improves maintainability and consistency.

`TodaysDate.jsx` is a simple component that displays the current date in the header, adding a professional touch and context for users.

The project’s folder structure is straightforward: all main components are in the `src/components` directory, with static assets in `public/`. The root `App.css` file contains custom styles, though most styling is handled by Tailwind CSS utility classes.

During development, several design choices were debated. For example, I considered using a backend for data persistence, but opted for local storage to keep the project simple and easy to deploy. I also debated between using a table or a grid for the stock list; a table was chosen for its clarity and ease of sorting/filtering. The decision to use TradingView widgets was made after evaluating several data sources, as TradingView offered the best combination of real-time data and visual appeal.

In summary, Stock Dashboard is a feature-rich, extensible platform for stock tracking and analysis. Its modular design, modern tech stack, and thoughtful UI make it a strong foundation for further development or customization. Whether you are building your first watchlist, exploring stock data visualization, or looking for a base to create your own finance app, Stock Dashboard provides the tools and flexibility you need.

For more information, to report issues, or to contribute, please visit the project’s GitHub repository. The project is open source and available under the MIT License.
