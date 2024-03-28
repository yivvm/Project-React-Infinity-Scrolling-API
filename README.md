# Book Search App

This React application allows users to search for books. It utilizes a custom hook `useBookSearch` to fetch book data based on user input.

## Features

- Search for books by typing in the input field.
- Infinite scrolling: Load more books as you scroll down the page.
- Loading indicator: Displays "Loading..." while fetching data.
- Error handling: Shows "Error" if there's an issue with fetching data.

## Installation

To run this application locally, follow these steps:

1. Clone this repository.
2. Navigate to the project directory.
3. Install dependencies by running `npm install` or `yarn install`.
4. Start the development server by running `npm start` or `yarn start`.
5. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Usage

1. Type your desired query into the search input.
2. As you type, the application will fetch and display relevant book results.
3. Scroll down to load more books automatically if available.

## Code Overview

The main logic for fetching book data and handling infinite scrolling is contained within the `App` component. Here's an overview of the code:

- `useState` is used to manage the state of the search query (`query`) and the current page number (`pageNumber`).
- The `useBookSearch` custom hook is used to fetch book data based on the search query and page number.
- `useRef` and `useCallback` are used to create an intersection observer that detects when the last book element is visible on the screen, triggering the loading of more books.
- The `handleSearch` function updates the search query state and resets the page number to 1 when the user types in the search input.
- Book data is displayed dynamically using `map()`, with a special `ref` assigned to the last book element to facilitate infinite scrolling.
- Loading and error states are displayed conditionally based on the hook's return values.

## Dependencies

This project relies on the following dependencies:

- `react`: ^17.0.2
- `react-dom`: ^17.0.2
- `useBookSearch`: Custom hook for fetching book data.

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

# Project-React-Infinity-Scrolling-API
