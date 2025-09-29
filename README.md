# foodio-backend

This is the backend server for the Foodio application. It fetches restaurant data from the Swiggy API and provides it to the frontend.

## Installation

1.  Clone the repository:
    ```bash
    git clone git@github.com:atharao/foodio-backend.git
    ```
2.  Install the dependencies:
    ```bash
    npm install
    ```

## Usage

### Development

To run the server in development mode with automatic reloading, use:

```bash
npm run dev
```

The server will be available at `http://localhost:5000`.

### Production

To run the server in production mode, use:

```bash
npm start
```

The server will be available at `http://localhost:5000`.

## API Endpoints

### Get Restaurant List

-   **URL:** `/api/restaurants`
-   **Method:** `GET`
-   **Description:** Fetches a list of restaurants.
-   **Success Response:**
    -   **Code:** 200
    -   **Content:** A JSON object containing the restaurant list.
-   **Error Response:**
    -   **Code:** 500
    -   **Content:** `{ "error": "Failed to fetch restaurants" }`

### Get Restaurant Menu

-   **URL:** `/api/restaurants/menu/:resId`
-   **Method:** `GET`
-   **Description:** Fetches the menu for a specific restaurant.
-   **URL Params:**
    -   `resId=[string]` (required) - The ID of the restaurant.
-   **Success Response:**
    -   **Code:** 200
    -   **Content:** A JSON object containing the restaurant menu.
-   **Error Response:**
    -   **Code:** 500
    -   **Content:** `{ "error": "Failed to fetch restaurant menu" }`
