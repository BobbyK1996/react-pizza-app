Project Requirements:

- User can order one or more pizzas from a menu.
- The application should require no user accounts and offer no login functionality. Users can just input their names before using the app.
- The pizza menu can be changed, meaning it has to be loaded from an API, which has already been created. -> DONE
- Users can add multiple pizzas to a cart before ordering.
- Ordering requires the user's name, phone number and address.
- GPS location should also be provided if possible.
- User's can mark their order as "priority", which costs an extra 20% of the cart total.
- Orders will be made sending a POST request with the order data, which includes the user data and selected pizzas, to the API.
- Payments are made on delivery, so no payment processing will be used.
- Each order will receive an unique ID that can be sent to the user. This can be used to search their order based on the ID.
- Users will be able to mark the order as "priority" post ordering.

Features:

1. User -> Global UI state -> No accounts, stays in-app
2. Menu -> Global remote state -> Menu fetched from API
3. Cart -> Global UI state -> No API request
4. Order -> Global remote state -> Data fetched and submitted to API

Pages Mapped to Features:

1.1. Homepage -> /
2.1. Pizza menu -> /menu
3.1. Cart -> /cart
4.1. Placing a new order -> /order/new
4.2. Looking up an order -> /order/:orderID

TechStack:

- Routing -> React Router
- Styling -> TailwindCSS
- Remote state management -> React Router -> render-as-you-fetch approach
- UI State management -> Redux
