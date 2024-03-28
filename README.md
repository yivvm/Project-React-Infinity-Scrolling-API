# Book Search App

This React application allows users to search for books. It utilizes a custom hook `useBookSearch` to fetch book data based on user input.  
This is a simple React application for searching books using the Open Library API. It dynamically loads more books as you scroll down the page.

## Features

Once the application is running, you can start searching for books by typing in the search bar. As you type, the application will dynamically fetch and display the matching books. You can scroll down the page to load more books.

- Search for books by typing in the search input.
- As you type, the application will fetch and display relevant book results.
- Infinite scrolling: Load more books automatically as you scroll down the page.
- Loading indicator: Displays "Loading..." while fetching data.
- Error handling: Shows "Error" if there's an issue with fetching data.

## Installation

To run this application locally, follow these steps:

1. Clone this repository.
2. Navigate to the project directory.
3. Install dependencies by running `npm install` or `yarn install`.
4. Start the development server by running `npm start` or `yarn start`.
5. Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

## Components

### app.js

This file contains the main component of the application. It handles user input, sends queries to the API, and displays the list of books.

### useBookSearch.js:

This custom hook is responsible for fetching book data from the Open Library API using axios. It manages loading state, error handling, and pagination.

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
