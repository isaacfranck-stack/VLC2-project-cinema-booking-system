# Cinema Ticket Booking System

A web application for browsing movies and booking cinema tickets. Users can search films, add them to a cart, and make reservations with real-time seat availability tracking.

## What the App Does

This application provides a complete ticket booking experience for a small cinema. Users can browse the movie catalog, check availability, add films to their cart, and book seats while the system automatically tracks remaining seats.

### Main Features

- **Movie Catalog**: Browse all available films displayed in a responsive card grid. Each card shows the movie poster, title, genre, ticket price, available seats, and ID.
- **Search & Filter**: Real-time search bar to filter movies by title. Results update instantly as you type.
- **Shopping Cart**: Add movies to your cart with the "Aggiungi" (Add) button. The cart counter and total price update dynamically.
- **Seat Reservation**: Book tickets with the "Prenota" (Book) button. The system checks seat availability in real-time and prevents overbooking.
- **Availability Management**: If a movie sells out or reaches its booking limit, the button automatically disables and shows "Esaurito" (Sold Out).
- **Dynamic Pricing**: Total expenses are calculated and displayed in real-time as items are added to the cart or booked.
- **Responsive UI**: Clean, card-based layout built with vanilla HTML, CSS, and JavaScript.

### User Flow

1. The user opens the app and sees a grid of movie cards loaded from the JSON database via REST API.
2. They can use the search bar to filter movies by title.
3. Clicking **"Aggiungi"** adds the movie to the shopping cart and updates the total price.
4. Clicking **"Prenota"** books a seat for that movie. The system checks if seats are still available.
5. If seats run out, the booking button becomes disabled and displays **"Esaurito"**.
6. The header shows live counters: films in cart, films booked, and total expenses.

## Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+), DOM Manipulation
- **Backend**: json-server (REST API)
- **Database**: JSON file (`db.json`)
- **HTTP Client**: Fetch API with async/await

## Project Structure

```
VLC2-project---FILM-INDIMENTICABILI-/
├── backend/
│   └── db.json              # Movies and bookings data
└── frontend/
    ├── index.html           # Main application page
    ├── style.css            # Stylesheet
    └── immagini/            # Movie poster assets
```

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS version)
- [Git](https://git-scm.com/)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/isaacfranck-stack/VLC2-project---FILM-INDIMENTICABILI-.git
   cd VLC2-project---FILM-INDIMENTICABILI-/film-indimenticabili
   ```

2. **Start the backend server**
   ```bash
   cd backend
   npx json-server --watch db.json --port 3001 --static ../frontend
   ```

3. **Open the app**
   - Go to `http://localhost:3001` in your browser

## API Endpoints

| Method | Endpoint    | Description                  |
|--------|-------------|------------------------------|
| GET    | `/movies`   | Retrieve all movies          |
| GET    | `/bookings` | Retrieve all bookings        |
| POST   | `/bookings` | Create a new booking         |

## Skills Demonstrated

- **Frontend Development**: Semantic HTML, responsive CSS, dynamic DOM manipulation with vanilla JavaScript
- **Asynchronous Programming**: Fetch API with async/await for server communication
- **State Management**: Handling cart data, booking state, and UI updates in real-time
- **Data Filtering**: Implementing live search functionality with array filter methods
- **Input Validation**: Preventing overbooking by checking seat availability before confirming reservations
- **Dynamic UI Updates**: Disabling buttons, updating counters, and calculating totals based on user interactions
- **REST API Integration**: Consuming a JSON-based REST backend

## Contact

- LinkedIn: [Isaac Franck Tiensi Happi](https://www.linkedin.com/in/isaac-franck-tiensi-happi-2b647022a/)
- Email: cunegohappi@gmail.com

---

*This project was built as part of a web development course at Engim Torino Artigianelli (600 hours).*
